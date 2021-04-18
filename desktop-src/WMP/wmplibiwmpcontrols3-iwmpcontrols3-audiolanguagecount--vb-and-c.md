---
title: IWMPControls3 audiolanguagecount (Eigenschaft)
description: Die audiolanguagecount-Eigenschaft ruft die Anzahl der unterstützten Audiosprachen ab.
ms.assetid: 92e2093f-435b-4427-9f85-8c8ae76e0e2d
keywords:
- audiolanguagecount-Eigenschaften Fenster Media Player
- audiolanguagecount-Eigenschaft, Windows Media Player, IWMPControls3-Schnittstelle
- IWMPControls3 Interface, Windows Media Player, audiolanguagecount (Eigenschaft)
topic_type:
- apiref
api_name:
- IWMPControls3.audioLanguageCount
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd397dec80a5ccb5f2085e3231782555efde8e39
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365779"
---
# <a name="iwmpcontrols3audiolanguagecount-property"></a>IWMPControls3:: audiolanguagecount (Eigenschaft)

Die **audiolanguagecount** -Eigenschaft ruft die Anzahl der unterstützten Audiosprachen ab.

## <a name="syntax"></a>Syntax


```CSharp
public System.Int32 audioLanguageCount {get; set;}
```


```VB

Public ReadOnly Property audioLanguageCount As System.Int32
```





## <a name="property-value"></a>Eigenschaftswert

Ein **System. Int32** -Wert, der die Anzahl unterstützter Audiosprachen ist.

## <a name="remarks"></a>Bemerkungen

Bei Windows Media-basierten Inhalten unterstützen Eigenschaften und Methoden im Zusammenhang mit der Sprachauswahl nur eine einzige Ausgabe.

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

[**IWMPControls3. currentaudiolanguage (VB und c#)**](wmplibiwmpcontrols3-iwmpcontrols3-currentaudiolanguage--vb-and-c.md)
</dt> <dt>

[**IWMPControls3. currentaudiolanguageindex (VB und c#)**](wmplibiwmpcontrols3-iwmpcontrols3-currentaudiolanguageindex--vb-and-c.md)
</dt> <dt>

[**IWMPControls3. getaudiolanguagedescription (VB und c#)**](wmplibiwmpcontrols3-iwmpcontrols3-getaudiolanguagedescription--vb-and-c.md)
</dt> <dt>

[**IWMPControls3. getaudiolanguageid (VB und c#)**](wmplibiwmpcontrols3-iwmpcontrols3-getaudiolanguageid--vb-and-c.md)
</dt> <dt>

[**IWMPControls3. getlanguagename (VB und c#)**](wmplibiwmpcontrols3-iwmpcontrols3-getlanguagename--vb-and-c.md)
</dt> </dl>

 

 





