---
title: Matrix5x4F Matrix5x4F(FLOAT, FLOAT, FLOAT, FLOAT, FLOAT, FLOAT, FLOAT, FLOAT, FLOAT, FLOAT, FLOAT, FLOAT, FLOAT, FLOAT, FLOAT, FLOAT, FLOAT, FLOAT, FLOAT, FLOAT, FLOAT, FLOAT) Konstruktor (D2d1 \_ helper.h)
description: Instanziiert eine neue Instanz einer Matrix5x4F-Klasse, die mit allen Gleitkommamatrixwerten initialisiert wird.
ms.assetid: 46C2741F-9E49-4ABD-9DA5-D4E6D3CA2B09
keywords:
- Matrix5x4F-Konstruktor Direct2D
- Matrix5x4F-Konstruktor Direct2D, Matrix5x4F-Schnittstelle
- Matrix5x4F-Schnittstelle Direct2D, Matrix5x4F-Konstruktor
topic_type:
- apiref
api_name:
- Matrix5x4F.Matrix5x4F
api_location:
- D2d1.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3626e4af5e51555779a2d14c731fbeb4a2ad30ce542ce2ca9447116332c9faea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119430630"
---
# <a name="matrix5x4fmatrix5x4ffloat-float-float-float-float-float-float-float-float-float-float-float-float-float-float-float-float-float-float-float-constructor"></a>Matrix5x4F::Matrix5x4F(FLOAT, FLOAT, FLOAT, FLOAT, FLOAT, FLOAT, FLOAT, FLOAT, FLOAT, FLOAT, FLOAT, FLOAT, FLOAT, FLOAT, FLOAT, FLOAT, FLOAT, FLOAT, FLOAT, FLOAT, FLOAT, FLOAT)

Instanziiert eine neue Instanz einer [**Matrix5x4F-Klasse,**](matrix5x4f.md) die mit allen Gleitkommamatrixwerten initialisiert wird.

## <a name="syntax"></a>Syntax


```C++
inline Matrix5x4F(
   FLOAT m11,
   FLOAT m12,
   FLOAT m13,
   FLOAT m14,
   FLOAT m21,
   FLOAT m22,
   FLOAT m23,
   FLOAT m24,
   FLOAT m31,
   FLOAT m32,
   FLOAT m33,
   FLOAT m34,
   FLOAT m41,
   FLOAT m42,
   FLOAT m43,
   FLOAT m44,
   FLOAT m51,
   FLOAT m52,
   FLOAT m53,
   FLOAT m54
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*m11* 
</dt> <dd>

Typ: **FLOAT**

Der Wert in der ersten Zeile und ersten Spalte der Matrix.

</dd> <dt>

*m12* 
</dt> <dd>

Typ: **FLOAT**

Der Wert in der ersten Zeile und zweiten Spalte der Matrix.

</dd> <dt>

*m13* 
</dt> <dd>

Typ: **FLOAT**

Der Wert in der ersten Zeile und dritten Spalte der Matrix.

</dd> <dt>

*m14* 
</dt> <dd>

Typ: **FLOAT**

Der Wert in der ersten Zeile und vierten Spalte der Matrix.

</dd> <dt>

*m21* 
</dt> <dd>

Typ: **FLOAT**

Der Wert in der zweiten Zeile und ersten Spalte der Matrix.

</dd> <dt>

*m22* 
</dt> <dd>

Typ: **FLOAT**

Der Wert in der zweiten Zeile und zweiten Spalte der Matrix.

</dd> <dt>

*m23* 
</dt> <dd>

Typ: **FLOAT**

Der Wert in der zweiten Zeile und dritten Spalte der Matrix.

</dd> <dt>

*m24* 
</dt> <dd>

Typ: **FLOAT**

Der Wert in der zweiten Zeile und vierten Spalte der Matrix.

</dd> <dt>

*m31* 
</dt> <dd>

Typ: **FLOAT**

Der Wert in der dritten Zeile und ersten Spalte der Matrix.

</dd> <dt>

*m32* 
</dt> <dd>

Typ: **FLOAT**

Der Wert in der dritten Zeile und zweiten Spalte der Matrix.

</dd> <dt>

*m33* 
</dt> <dd>

Typ: **FLOAT**

Der Wert in der dritten Zeile und dritten Spalte der Matrix.

</dd> <dt>

*m34* 
</dt> <dd>

Typ: **FLOAT**

Der Wert in der dritten Zeile und vierten Spalte der Matrix.

</dd> <dt>

*m41* 
</dt> <dd>

Typ: **FLOAT**

Der Wert in der vierten Zeile und ersten Spalte der Matrix.

</dd> <dt>

*m42* 
</dt> <dd>

Typ: **FLOAT**

Der Wert in der vierten Zeile und zweiten Spalte der Matrix.

</dd> <dt>

*m43* 
</dt> <dd>

Typ: **FLOAT**

Der Wert in der vierten Zeile und dritten Spalte der Matrix.

</dd> <dt>

*m44* 
</dt> <dd>

Typ: **FLOAT**

Der Wert in der vierten Zeile und vierten Spalte der Matrix.

</dd> <dt>

*m51* 
</dt> <dd>

Typ: **FLOAT**

Der Wert in der fünften Zeile und ersten Spalte der Matrix.

</dd> <dt>

*m52* 
</dt> <dd>

Typ: **FLOAT**

Der Wert in der fünften Zeile und zweiten Spalte der Matrix.

</dd> <dt>

*m53* 
</dt> <dd>

Typ: **FLOAT**

Der Wert in der fünften Zeile und dritten Spalte der Matrix.

</dd> <dt>

*m54* 
</dt> <dd>

Typ: **FLOAT**

Der Wert in der fünften Zeile und vierten Spalte der Matrix.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7, Windows Vista mit SP2 und Plattformupdate nur für Windows \[ Vista-Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 R2, Windows Server 2008 mit SP2 und Plattformupdate nur für Windows Server \[ 2008-Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Telefon)<br/>  | Windows Phone 8.1 \[ Windows Phone Silverlight 8.1- und Windows Runtime-Apps\]<br/>                                           |
| Namespace<br/>                | D2D1<br/>                                                                                                                   |
| Header<br/>                   | <dl> <dt>D2d1 \_ helper.h</dt> </dl>                                         |
| Bibliothek<br/>                  | <dl> <dt>D2d1.lib</dt> </dl>                                               |
| DLL<br/>                      | <dl> <dt>D2d1.dll</dt> </dl>                                               |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Matrix5x4F**](matrix5x4f.md)
</dt> </dl>

 

 





