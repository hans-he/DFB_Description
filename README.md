DFB_Description
===============

showing the drawing flags and blitting flags in DirectFB1.4.

A simple program in processing.

Drawing flags
 DSDRAW_NOFX                  uses none of the effects
 DSDRAW_BLEND                 uses alpha from color
 DSDRAW_DST_COLORKEY          write to destination only if the destination pixel matches the destination color key
 DSDRAW_SRC_PREMULTIPLY       multiplies the color's rgb channels by the alpha channel before drawing
 DSDRAW_DST_PREMULTIPLY       modulates the dest. color with the dest. alpha
 DSDRAW_DEMULTIPLY            divides the color by the alpha before writing the data to the destination
 DSDRAW_XOR                   bitwise xor the destination pixels with the specified color after premultiplication

  7 scenarios to demonstration and 1 for trying.

Blitting flags
 DSBLIT_NOFX                  uses none of the effects
 DSBLIT_BLEND_ALPHACHANNEL    enables blending and uses alphachannel from source
 DSBLIT_BLEND_COLORALPHA      enables blending and uses alpha value from color
 DSBLIT_COLORIZE              modulates source color with the color's r/g/b values
 DSBLIT_SRC_COLORKEY          don't blit pixels matching the source color key
 DSBLIT_DST_COLORKEY          write to destination only if the destination pixel matches the destination color key
 DSBLIT_SRC_PREMULTIPLY       modulates the source color with the (modulated) source alpha
 DSBLIT_DST_PREMULTIPLY       modulates the dest. color with the dest. alpha
 DSBLIT_DEMULTIPLY            divides the color by the alpha before writing the data to the destination
 DSBLIT_DEINTERLACE           deinterlaces the source during blitting by reading only one field 
                              (every second line of full image) scaling it vertically by factor two
 DSBLIT_SRC_PREMULTCOLOR      modulates the source color with the color alpha
 DSBLIT_XOR                   bitwise xor the destination pixels with the source pixels after premultiplication
 DSBLIT_INDEX_TRANSLATION     do fast indexed to indexed translation, this flag is mutual exclusive with all others
 DSBLIT_ROTATE90              rotate the image by 90 degree
 DSBLIT_ROTATE180             rotate the image by 180 degree
 DSBLIT_ROTATE270             rotate the image by 270 degree
 DSBLIT_COLORKEY_PROTECT      make sure written pixels don't match color key (internal only ATM)
 DSBLIT_SRC_MASK_ALPHA        modulate source alpha channel with alpha channel from source mask, 
                              see also IDirectFBSurface::SetSourceMask()
 DSBLIT_SRC_MASK_COLOR        modulate source color channels with color channels from source mask, 
                              see also IDirectFBSurface::SetSourceMask()
 DSBLIT_SOURCE2               use secondary source instead of destination for reading
 DSBLIT_FLIP_HORIZONTAL       flip the image horizontally
 DSBLIT_FLIP_VERTICAL         flip the image vertically 
 
  22 scenarios to demonstration and 1 for trying.
