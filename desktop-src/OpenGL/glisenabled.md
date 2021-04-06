---
title: glisenabled-Funktion (GL. h)
description: Die gllsenabled-Funktion testet, ob eine Funktion aktiviert ist.
ms.assetid: 18df5a6f-dc21-434d-a2e8-2c58597df037
keywords:
- glisenabled-Funktion OpenGL
topic_type:
- apiref
api_name:
- glIsEnabled
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8fdb2ba206e0a026aef118b06d66097ade9ba9ac
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743128"
---
# <a name="glisenabled-function"></a>glisenabled-Funktion

Die **gllsenabled** -Funktion testet, ob eine Funktion aktiviert ist.

## <a name="syntax"></a>Syntax


```C++
GLboolean WINAPI glIsEnabled(
   GLenum cap
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Decke* 
</dt> <dd>

Eine symbolische Konstante, die eine OpenGL-Funktion angibt. Die folgenden Funktionen werden akzeptiert.



| Wert                                                                                                                                                                                                    | Bedeutung                                                                                                                                             |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_ALPHA_TEST"></span><span id="gl_alpha_test"></span><dl> <dt>**GL- \_ alpha \_ Test**</dt> </dl>                                           | Siehe [ **glalphafunc**](glalphafunc.md)<br/>                                                                                                   |
| <span id="GL_AUTO_NORMAL"></span><span id="gl_auto_normal"></span><dl> <dt>**GL \_ Auto \_ Normal**</dt> </dl>                                        | Siehe [ **glevalcoord**](glevalcoord-functions.md)<br/>                                                                                         |
| <span id="GL_BLEND"></span><span id="gl_blend"></span><dl> <dt>**GL \_ Blend**</dt> </dl>                                                           | Siehe [ **glblendfunc**](glblendfunc.md)<br/>                                                                                                   |
| <span id="GL_CLIP_PLANE_i"></span><span id="gl_clip_plane_i"></span><span id="GL_CLIP_PLANE_I"></span><dl> <dt>* * GL \_ - \_ clippinbene * i * * *</dt> </dl> | Siehe [ **glclipplane**](glclipplane.md)<br/>                                                                                                   |
| <span id="GL_COLOR_ARRAY"></span><span id="gl_color_array"></span><dl> <dt>**GL \_ - \_ Farbarray**</dt> </dl>                                        | Siehe [ **glcolorpointer**](glcolorpointer.md)<br/>                                                                                             |
| <span id="GL_COLOR_LOGIC_OP"></span><span id="gl_color_logic_op"></span><dl> <dt>**GL- \_ Farb \_ Logik- \_ op**</dt> </dl>                              | Siehe [ **gllogicop**](gllogicop.md)<br/>                                                                                                       |
| <span id="GL_COLOR_MATERIAL"></span><span id="gl_color_material"></span><dl> <dt>**GL- \_ Farb \_ Material**</dt> </dl>                               | Siehe [ **glcolormaterial**](glcolormaterial.md)<br/>                                                                                           |
| <span id="GL_CULL_FACE"></span><span id="gl_cull_face"></span><dl> <dt>**GL. Ober \_ \_ Fläche**</dt> </dl>                                              | Siehe [ **glcullface**](glcullface.md)<br/>                                                                                                     |
| <span id="GL_DEPTH_TEST"></span><span id="gl_depth_test"></span><dl> <dt>**GL- \_ tiefen \_ Test**</dt> </dl>                                           | Siehe " [**gldepthfunc**](gldepthfunc.md) " und " [**gldepthrange**](gldepthrange.md) ".<br/>                                                          |
| <span id="GL_DITHER"></span><span id="gl_dither"></span><dl> <dt>**GL \_ .**</dt> </dl>                                                        | Siehe [ **glEnable**](glenable.md)<br/>                                                                                                         |
| <span id="GL_FOG"></span><span id="gl_fog"></span><dl> <dt>**GL- \_ Nebel**</dt> </dl>                                                                 | Siehe [ **glnebel**](glfog.md)<br/>                                                                                                               |
| <span id="GL_INDEX_ARRAY"></span><span id="gl_index_array"></span><dl> <dt>**GL- \_ Index \_ Array**</dt> </dl>                                        | Siehe [ **glindexpointer**](glindexpointer.md)<br/>                                                                                             |
| <span id="GL_INDEX_LOGIC_OP"></span><span id="gl_index_logic_op"></span><dl> <dt>**GL- \_ Index \_ Logik- \_ op**</dt> </dl>                              | Siehe [ **gllogicop**](gllogicop.md)<br/>                                                                                                       |
| <span id="GL_LIGHT_i"></span><span id="gl_light_i"></span><span id="GL_LIGHT_I"></span><dl> <dt>* * GL \_ Light * i * * *</dt> </dl>                      | Siehe [**gllightmodel**](gllightmodel-functions.md) und [**gllight**](gllight-functions.md)<br/>                                              |
| <span id="GL_LIGHTING"></span><span id="gl_lighting"></span><dl> <dt>**GL- \_ Beleuchtung**</dt> </dl>                                                  | Siehe [**glmaterial**](glmaterial-functions.md), [**gllightmodel**](gllightmodel-functions.md)und [**gllight**](gllight-functions.md)<br/> |
| <span id="GL_LINE_SMOOTH"></span><span id="gl_line_smooth"></span><dl> <dt>**GL- \_ Linie \_ glatt**</dt> </dl>                                        | Siehe [ **glLineWidth**](gllinewidth.md)<br/>                                                                                                   |
| <span id="GL_LINE_STIPPLE"></span><span id="gl_line_stipple"></span><dl> <dt>**GL- \_ Zeilen \_ Stippel**</dt> </dl>                                     | Siehe [ **gllinestippel**](gllinestipple.md)<br/>                                                                                               |
| <span id="GL_MAP1_COLOR_4"></span><span id="gl_map1_color_4"></span><dl> <dt>**GL \_ zuordnung1 \_ Farbe \_ 4**</dt> </dl>                                    | Siehe [ **glMap1**](glmap1.md)<br/>                                                                                                             |
| <span id="GL_MAP1_INDEX"></span><span id="gl_map1_index"></span><dl> <dt>**GL \_ zuordnung1 \_ Index**</dt> </dl>                                           | Siehe [ **glMap1**](glmap1.md)<br/>                                                                                                             |
| <span id="GL_MAP1_NORMAL"></span><span id="gl_map1_normal"></span><dl> <dt>**GL \_ zuordnung1 \_ Normal**</dt> </dl>                                        | Siehe [ **glMap1**](glmap1.md)<br/>                                                                                                             |
| <span id="GL_MAP1_TEXTURE_COORD_1"></span><span id="gl_map1_texture_coord_1"></span><dl> <dt>**GL \_ zuordnung1 \_ Textur \_ Koord \_ 1**</dt> </dl>           | Siehe [ **glMap1**](glmap1.md)<br/>                                                                                                             |
| <span id="GL_MAP1_TEXTURE_COORD_2"></span><span id="gl_map1_texture_coord_2"></span><dl> <dt>**GL \_ zuordnung1 \_ Textur- \_ Koord \_ 2**</dt> </dl>           | Siehe [ **glMap1**](glmap1.md)<br/>                                                                                                             |
| <span id="GL_MAP1_TEXTURE_COORD_3"></span><span id="gl_map1_texture_coord_3"></span><dl> <dt>**GL \_ zuordnung1 \_ Textur \_ Koord \_ 3**</dt> </dl>           | Siehe [ **glMap1**](glmap1.md)<br/>                                                                                                             |
| <span id="GL_MAP1_TEXTURE_COORD_4"></span><span id="gl_map1_texture_coord_4"></span><dl> <dt>**GL \_ zuordnung1 \_ Textur- \_ Koord \_ 4**</dt> </dl>           | Siehe [ **glMap1**](glmap1.md)<br/>                                                                                                             |
| <span id="GL_MAP1_VERTEX_3"></span><span id="gl_map1_vertex_3"></span><dl> <dt>**GL \_ zuordnung1 \_ Scheitelpunkt \_ 3**</dt> </dl>                                 | Siehe [ **glMap1**](glmap1.md)<br/>                                                                                                             |
| <span id="GL_MAP1_VERTEX_4"></span><span id="gl_map1_vertex_4"></span><dl> <dt>**GL \_ zuordnung1 \_ Scheitelpunkt \_ 4**</dt> </dl>                                 | Siehe [ **glMap1**](glmap1.md)<br/>                                                                                                             |
| <span id="GL_MAP2_COLOR_4"></span><span id="gl_map2_color_4"></span><dl> <dt>**GL \_ map2 \_ Farbe \_ 4**</dt> </dl>                                    | Siehe [ **glMap2**](glmap2.md)<br/>                                                                                                             |
| <span id="GL_MAP2_INDEX"></span><span id="gl_map2_index"></span><dl> <dt>**GL \_ map2 \_ Index**</dt> </dl>                                           | Siehe [ **glMap2**](glmap2.md)<br/>                                                                                                             |
| <span id="GL_MAP2_NORMAL"></span><span id="gl_map2_normal"></span><dl> <dt>**GL \_ map2 \_ Normal**</dt> </dl>                                        | Siehe [ **glMap2**](glmap2.md)<br/>                                                                                                             |
| <span id="GL_MAP2_TEXTURE_COORD_1"></span><span id="gl_map2_texture_coord_1"></span><dl> <dt>**GL \_ map2 \_ Textur \_ Koord \_ 1**</dt> </dl>           | Siehe [ **glMap2**](glmap2.md)<br/>                                                                                                             |
| <span id="GL_MAP2_TEXTURE_COORD_2"></span><span id="gl_map2_texture_coord_2"></span><dl> <dt>**GL \_ map2 \_ Textur- \_ Koord \_ 2**</dt> </dl>           | Siehe [ **glMap2**](glmap2.md)<br/>                                                                                                             |
| <span id="GL_MAP2_TEXTURE_COORD_3"></span><span id="gl_map2_texture_coord_3"></span><dl> <dt>**GL \_ map2 \_ Textur \_ Koord \_ 3**</dt> </dl>           | Siehe [ **glMap2**](glmap2.md)<br/>                                                                                                             |
| <span id="GL_MAP2_TEXTURE_COORD_4"></span><span id="gl_map2_texture_coord_4"></span><dl> <dt>**GL \_ map2 \_ Textur- \_ Koord \_ 4**</dt> </dl>           | Siehe [ **glMap2**](glmap2.md)<br/>                                                                                                             |
| <span id="GL_MAP2_VERTEX_3"></span><span id="gl_map2_vertex_3"></span><dl> <dt>**GL \_ map2 \_ Scheitelpunkt \_ 3**</dt> </dl>                                 | Siehe [ **glMap2**](glmap2.md)<br/>                                                                                                             |
| <span id="GL_MAP2_VERTEX_4"></span><span id="gl_map2_vertex_4"></span><dl> <dt>**GL \_ map2 \_ Scheitelpunkt \_ 4**</dt> </dl>                                 | Siehe [ **glMap2**](glmap2.md)<br/>                                                                                                             |
| <span id="GL_NORMAL_ARRAY"></span><span id="gl_normal_array"></span><dl> <dt>**GL- \_ normales \_ Array**</dt> </dl>                                     | Siehe [ **glnormalpointer**](glnormalpointer.md)<br/>                                                                                           |
| <span id="GL_NORMALIZE"></span><span id="gl_normalize"></span><dl> <dt>**GL \_ normalize**</dt> </dl>                                               | Siehe [ **glnormal**](glnormal-functions.md)<br/>                                                                                               |
| <span id="GL_POINT_SMOOTH"></span><span id="gl_point_smooth"></span><dl> <dt>**GL- \_ Punkt \_ glatt**</dt> </dl>                                     | Siehe [ **glPointSize**](glpointsize.md)<br/>                                                                                                   |
| <span id="GL_POLYGON_OFFSET_FILL"></span><span id="gl_polygon_offset_fill"></span><dl> <dt>**GL- \_ Polygon- \_ Offset \_ Füllung**</dt> </dl>               | Siehe [ **glpolygonoffset**](glpolygonoffset.md)<br/>                                                                                           |
| <span id="GL_POLYGON_OFFSET_LINE"></span><span id="gl_polygon_offset_line"></span><dl> <dt>**GL- \_ Polygon- \_ Offset \_ Linie**</dt> </dl>               | Siehe [ **glpolygonoffset**](glpolygonoffset.md)<br/>                                                                                           |
| <span id="GL_POLYGON_OFFSET_POINT"></span><span id="gl_polygon_offset_point"></span><dl> <dt>**GL- \_ Polygon- \_ Offset \_ Punkt**</dt> </dl>            | Siehe [ **glpolygonoffset**](glpolygonoffset.md)<br/>                                                                                           |
| <span id="GL_POLYGON_SMOOTH"></span><span id="gl_polygon_smooth"></span><dl> <dt>**GL- \_ Polygon \_ glatt**</dt> </dl>                               | Siehe [ **glpolygonmode**](glpolygonmode.md)<br/>                                                                                               |
| <span id="GL_POLYGON_STIPPLE"></span><span id="gl_polygon_stipple"></span><dl> <dt>**GL- \_ Polygon- \_ Stippel**</dt> </dl>                            | Siehe [ **glpolygonstippel**](glpolygonstipple.md)<br/>                                                                                         |
| <span id="GL_SCISSOR_TEST"></span><span id="gl_scissor_test"></span><dl> <dt>**GL- \_ Scissor- \_ Test**</dt> </dl>                                     | Siehe [ **glscissor**](glscissor.md)<br/>                                                                                                       |
| <span id="GL_STENCIL_TEST"></span><span id="gl_stencil_test"></span><dl> <dt>**GL- \_ Schablonen \_ Test**</dt> </dl>                                     | Siehe [**glstencilfunc**](glstencilfunc.md) und [**glstencilop**](glstencilop.md)<br/>                                                        |
| <span id="GL_TEXTURE_1D"></span><span id="gl_texture_1d"></span><dl> <dt>**GL \_ \_ -Textur 1D**</dt> </dl>                                           | Siehe [ **glTexImage1D**](glteximage1d.md)<br/>                                                                                                 |
| <span id="GL_TEXTURE_2D"></span><span id="gl_texture_2d"></span><dl> <dt>**GL \_ Textur \_ 2D**</dt> </dl>                                           | Siehe [ **glTexImage2D**](glteximage2d.md)<br/>                                                                                                 |
| <span id="GL_TEXTURE_COORD_ARRAY"></span><span id="gl_texture_coord_array"></span><dl> <dt>**GL- \_ Textur \_ Koord- \_ Array**</dt> </dl>               | Siehe [ **gltexcoordpointer**](gltexcoordpointer.md)<br/>                                                                                       |
| <span id="GL_TEXTURE_GEN_Q"></span><span id="gl_texture_gen_q"></span><dl> <dt>**GL \_ Textur \_ gen, \_ Q**</dt> </dl>                                 | Siehe [ **gltexgen**](gltexgen-functions.md)<br/>                                                                                               |
| <span id="GL_TEXTURE_GEN_R"></span><span id="gl_texture_gen_r"></span><dl> <dt>**GL \_ Textur \_ gen \_ R**</dt> </dl>                                 | Siehe [ **gltexgen**](gltexgen-functions.md)<br/>                                                                                               |
| <span id="GL_TEXTURE_GEN_S"></span><span id="gl_texture_gen_s"></span><dl> <dt>**GL- \_ Textur \_ gen \_ S**</dt> </dl>                                 | Siehe [ **gltexgen**](gltexgen-functions.md)<br/>                                                                                               |
| <span id="GL_TEXTURE_GEN_T"></span><span id="gl_texture_gen_t"></span><dl> <dt>**GL \_ Textur \_ gen \_ T**</dt> </dl>                                 | Siehe [ **gltexgen**](gltexgen-functions.md)<br/>                                                                                               |
| <span id="GL_VERTEX_ARRAY"></span><span id="gl_vertex_array"></span><dl> <dt>**GL- \_ Scheitelpunkt \_ Array**</dt> </dl>                                     | Siehe [ **glvertexpointer**](glvertexpointer.md)<br/>                                                                                           |



 

</dd> </dl>

## <a name="error-codes"></a>Fehlercodes

Die folgenden Fehlercodes können von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.



| Name                                                                                                  | Bedeutung                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ ungültige Aufzählung. \_**</dt> </dl>      | die *Obergrenze* war kein akzeptierter Wert.<br/>                                                                                           |
| <dl> <dt>**\_ungültiger \_ Vorgang**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.<br/> |



## <a name="remarks"></a>Bemerkungen

Die **gllsenabled** -Funktion gibt "GL true" zurück, \_ Wenn " *Cap* " eine aktivierte Funktion ist, andernfalls "GL \_ false"

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                              |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>GL. h</dt> </dl>         |
| Bibliothek<br/>                  | <dl> <dt>Opengl32. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Opengl32.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**glBegin**](glbegin.md)
</dt> <dt>

[**glEnable**](glenable.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> </dl>

 

 





