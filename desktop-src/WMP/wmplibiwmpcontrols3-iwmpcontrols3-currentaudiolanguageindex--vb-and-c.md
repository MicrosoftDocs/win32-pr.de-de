---
title: IWMPControls3 currentaudiolanguageindex (Eigenschaft)
description: Die currentaudiolanguageindex-Eigenschaft ruft den 1-basierten Index ab, der der Audiosprache für die Wiedergabe entspricht, oder legt ihn fest.
ms.assetid: 3ed60827-c4e9-4455-b95e-b6eebf7a9a08
keywords:
- currentaudiolanguageindex-Eigenschaft, Fenster Media Player
- currentaudiolanguageindex-Eigenschaft, Windows Media Player, IWMPControls3-Schnittstelle
- IWMPControls3 Interface Windows Media Player, currentaudiolanguageindex (Eigenschaft)
topic_type:
- apiref
api_name:
- IWMPControls3.currentAudioLanguageIndex
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4fb36eea4038322cacd7f233892151ab77e5eea
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369245"
---
# <a name="iwmpcontrols3currentaudiolanguageindex-property"></a>IWMPControls3:: currentaudiolanguageindex (Eigenschaft)

Die **currentaudiolanguageindex** -Eigenschaft ruft den 1-basierten Index ab, der der Audiosprache für die Wiedergabe entspricht, oder legt ihn fest.

## <a name="syntax"></a>Syntax


```CSharp
public System.Int32 currentAudioLanguageIndex {get; set;}
```


```VB

Public Property currentAudioLanguageIndex As System.Int32
```





## <a name="property-value"></a>Eigenschaftswert

Ein **System. Int32** -Wert, der der einbasierte Index der Sprache ist.

## <a name="remarks"></a>Bemerkungen

Bei Windows Media-basierten Inhalten unterstützen Eigenschaften und Methoden im Zusammenhang mit der Sprachauswahl nur eine einzige Ausgabe.

Verwenden Sie die Eigenschaft **audiolanguagecount** , um die Anzahl der unterstützten Audiosprachen abzurufen.

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

[**IWMPControls3. getaudiolanguagedescription (VB und c#)**](wmplibiwmpcontrols3-iwmpcontrols3-getaudiolanguagedescription--vb-and-c.md)
</dt> <dt>

[**IWMPControls3. getaudiolanguageid (VB und c#)**](wmplibiwmpcontrols3-iwmpcontrols3-getaudiolanguageid--vb-and-c.md)
</dt> <dt>

[**IWMPControls3. getlanguagename (VB und c#)**](wmplibiwmpcontrols3-iwmpcontrols3-getlanguagename--vb-and-c.md)
</dt> </dl>

 

 





