---
title: IWMPClosedCaption SAMIFileName (Eigenschaft)
description: Die SAMIFileName-Eigenschaft ruft den Namen einer Datei ab, die die für die Untertitelung erforderlichen Informationen enthält, oder legt diesen fest.
ms.assetid: c3162c5f-9d66-41d4-920c-ed9840742d9d
keywords:
- SAMIFileName-Windows Media Player
- SAMIFileName-Eigenschaft Windows Media Player , IWMPClosedCaption-Schnittstelle
- IWMPClosedCaption-Schnittstelle Windows Media Player , SAMIFileName-Eigenschaft
topic_type:
- apiref
api_name:
- IWMPClosedCaption.SAMIFileName
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 973b0757eca4251e74180d829205ee6c7080ca821db2eeada3abc825bb4b5073
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117930323"
---
# <a name="iwmpclosedcaptionsamifilename-property"></a>IWMPClosedCaption::SAMIFileName (Eigenschaft)

Die **SAMIFileName-Eigenschaft** ruft den Namen einer Datei ab, die die für die Untertitelung erforderlichen Informationen enthält, oder legt diesen fest.

## <a name="syntax"></a>Syntax


```CSharp
public System.String SAMIFileName {get; set;}
```


```VB

Public Property SAMIFileName As System.String
```





## <a name="property-value"></a>Eigenschaftswert

Die **System.String-Datei,** die der Name der SAMI-Datei (Synchronized Accessible Media Interchange) ist.

## <a name="remarks"></a>Hinweise

Die SAMI-Datei muss eine SMI- oder SAMI-Dateierweiterung verwenden.

Wenn Sie keinen Wert mit **SAMIFileName** festlegen,  ruft diese Eigenschaft eine Zeichenfolge ab, die den Standarddateinamen oder die URL enthält, die dem aktuellen Medienelement zugeordnet ist. Diese Zuordnung kann auftreten, wenn eine SAMI-Datei mithilfe des *sami-URL-Parameters* angegeben wird, oder automatisch, wenn die SAMI-Datei denselben Namen wie die digitale Mediendatei hat (mit Ausnahme der Dateierweiterung). Wenn dem aktuellen Medium keine SAMI-Standarddatei zugeordnet ist, erhält diese Eigenschaft eine Zeichenfolge der Länge 0 ("").

Nachdem Sie einen Wert mithilfe von **SAMIFileName** festgelegt haben, wird dieser Wert beibehalten, bis Sie einen neuen Wert festlegen (oder bis ein neues Medienelement mithilfe des Sami-URL-Parameters geöffnet wird). Daher müssen Sie einen neuen Wert für diese Eigenschaft festlegen, bevor Sie jedes neue Medienelement wieder geben. Auf diese Weise wird der neue Wert für **SAMIFileName** wirksam, wenn das nächste Medienelement geöffnet wird (oder **wenn AxWindowsMediaPlayer.close** aufgerufen wird). Die Angabe eines neuen Werts **für SAMIFileName** hat keine Auswirkungen auf das aktuelle Medium.

Damit Windows Media Player SAMI-Standarddatei verwendet, die einem bestimmten Medienelement zugeordnet ist, legen Sie **SAMIFileName** auf eine Zeichenfolge der Länge 0 ("") fest, bevor Sie das nächste Medienelement wiedergibt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 9er Serie oder höher<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Hinzufügen von Untertiteln zu digitalen Medien**](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[**AxWindowsMediaPlayer.close**](axwmplib-axwindowsmediaplayer-close.md)
</dt> <dt>

[**IWMPClosedCaption-Schnittstelle (VB und C#)**](iwmpclosedcaption--vb-and-c.md)
</dt> <dt>

[**IWMPClosedCaption2-Schnittstelle (VB und C#)**](iwmpclosedcaption2--vb-and-c.md)
</dt> </dl>

 

 





