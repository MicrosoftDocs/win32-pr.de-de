---
title: IWMPControls3 getaudiolanguageid-Methode
description: Die getaudiolanguageid-Methode gibt den Gebiets Schema Bezeichner (Locale Identifier, LCID) für einen angegebenen audiosprachindex zurück.
ms.assetid: 880bbfca-6f69-41ce-a078-467c1939fae5
keywords:
- getaudiolanguageid-Methode, Windows Media Player
- getaudiolanguageid-Methode, Windows Media Player, IWMPControls3-Schnittstelle
- IWMPControls3 Interface, Windows Media Player, getaudiolanguageid-Methode
topic_type:
- apiref
api_name:
- IWMPControls3.getAudioLanguageID
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb8112eafec018b12012d20b37bfe30f7b464377
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370803"
---
# <a name="iwmpcontrols3getaudiolanguageid-method"></a>IWMPControls3:: getaudiolanguageid-Methode

Die **getaudiolanguageid** -Methode gibt den Gebiets Schema Bezeichner (Locale Identifier, LCID) für einen angegebenen audiosprachindex zurück.

## <a name="syntax"></a>Syntax


```CSharp
public System.Int32 getAudioLanguageID(
  System.Int32 lIndex
);
```


```VB

Public Function getAudioLanguageID( _
  ByVal lIndex As System.Int32 _
) As System.Int32
Implements IWMPControls3.getAudioLanguageID
```





## <a name="parameters"></a>Parameter

<dl> <dt>

*Lindex* \[ in\]
</dt> <dd>

Ein **System. Int32** -Wert, der der einbasierte Index der Audiosprache ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Ein **System. Int32** -Wert, der die LCID ist.

## <a name="remarks"></a>Bemerkungen

Eine LCID identifiziert eindeutig einen bestimmten Sprach Dialekt, der als Gebiets Schema bezeichnet wird.

Bei Windows Media-basierten Inhalten unterstützen Eigenschaften und Methoden im Zusammenhang mit der Sprachauswahl nur eine einzige Ausgabe.

Verwenden Sie die Eigenschaft **audiolanguagecount** , um die Anzahl der unterstützten Audiosprachen abzurufen, und greifen Sie dann einzeln mithilfe eines 1-basierten Indexes auf eine Audiosprache zu.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 9-Serie oder höher<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IWMPControls3-Schnittstelle (VB und c#)**](iwmpcontrols3--vb-and-c.md)
</dt> <dt>

[**IWMPControls3. audiolanguagecount (VB und c#)**](wmplibiwmpcontrols3-iwmpcontrols3-audiolanguagecount--vb-and-c.md)
</dt> <dt>

[**IWMPControls3. currentaudiolanguage (VB und c#)**](wmplibiwmpcontrols3-iwmpcontrols3-currentaudiolanguage--vb-and-c.md)
</dt> <dt>

[**IWMPControls3. currentaudiolanguageindex (VB und c#)**](wmplibiwmpcontrols3-iwmpcontrols3-currentaudiolanguageindex--vb-and-c.md)
</dt> <dt>

[**IWMPControls3. getaudiolanguagedescription (VB und c#)**](wmplibiwmpcontrols3-iwmpcontrols3-getaudiolanguagedescription--vb-and-c.md)
</dt> <dt>

[**IWMPControls3. getlanguagename (VB und c#)**](wmplibiwmpcontrols3-iwmpcontrols3-getlanguagename--vb-and-c.md)
</dt> </dl>

 

 





