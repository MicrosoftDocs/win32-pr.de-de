---
title: Iwmpclosedcaption samifilename (Eigenschaft)
description: Die samifilename-Eigenschaft ruft den Namen einer Datei ab, die die für den Untertitel erforderlichen Informationen enthält, oder legt ihn fest.
ms.assetid: c3162c5f-9d66-41d4-920c-ed9840742d9d
keywords:
- Samifilename-Eigenschaft, Windows-Media Player
- Samifilename-Eigenschaft, Windows Media Player, iwmpclosedcaption-Schnittstelle
- Iwmpclosedcaption-Schnittstelle, Windows Media Player, samifilename (Eigenschaft)
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
ms.openlocfilehash: d251f2bbf0c8839ab9a0005c69e1869c47af16ef
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106351368"
---
# <a name="iwmpclosedcaptionsamifilename-property"></a>Iwmpclosedcaption:: samifilename (Eigenschaft)

Die **samifilename** -Eigenschaft ruft den Namen einer Datei ab, die die für den Untertitel erforderlichen Informationen enthält, oder legt ihn fest.

## <a name="syntax"></a>Syntax


```CSharp
public System.String SAMIFileName {get; set;}
```


```VB

Public Property SAMIFileName As System.String
```





## <a name="property-value"></a>Eigenschaftswert

" **System. String** " ist der Name der synchronisierten, zugänglichen Medienaustausch Datei (Sami).

## <a name="remarks"></a>Bemerkungen

Die Sami-Datei muss eine SMI-oder. Sami-Dateinamenerweiterung verwenden.

Wenn Sie keinen Wert mit **samifilename** festlegen, ruft diese Eigenschaft eine **Zeichenfolge** ab, die den Standard Dateinamen oder die URL enthält, die dem aktuellen Medien Element zugeordnet ist. Diese Zuordnung kann auftreten, wenn eine Sami-Datei mithilfe des *Sami* URL-Parameters angegeben wird, oder automatisch, wenn die Sami-Datei den gleichen Namen wie die digitale Mediendatei hat (mit Ausnahme der Dateinamenerweiterung). Wenn dem aktuellen Medium keine Standard-Sami-Datei zugeordnet ist, erhält diese Eigenschaft eine Zeichenfolge der Länge 0 (null) ("").

Nachdem Sie einen Wert mit **samifilename** festgelegt haben, wird dieser Wert beibehalten, bis Sie einen neuen Wert festlegen (oder bis ein neues Medien Element mithilfe des Sami URL-Parameters geöffnet wird). Daher müssen Sie vor jedem neuen Medien Element einen neuen Wert für diese Eigenschaft festlegen. Auf diese Weise wird der neue Wert für **samifilename** wirksam, wenn das nächste Medien Element geöffnet wird (oder wenn **AxWindowsMediaPlayer. Close** aufgerufen wird). Das Angeben eines neuen Werts für **samifilename** hat keine Auswirkung auf das aktuelle Medium.

Legen Sie **samifilename** auf eine Zeichenfolge der Länge 0 ("") fest, bevor Sie das nächste Medien Element wiedergeben, damit Windows Media Player die einem bestimmten Medien Element zugeordnete standardmäßige Sami-Datei verwendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 9-Serie oder höher<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Hinzufügen von Untertiteln zu digitalen Medien**](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[**AxWindowsMediaPlayer. Close**](axwmplib-axwindowsmediaplayer-close.md)
</dt> <dt>

[**Iwmpclosedcaption-Schnittstelle (VB und c#)**](iwmpclosedcaption--vb-and-c.md)
</dt> <dt>

[**IWMPClosedCaption2-Schnittstelle (VB und c#)**](iwmpclosedcaption2--vb-and-c.md)
</dt> </dl>

 

 





