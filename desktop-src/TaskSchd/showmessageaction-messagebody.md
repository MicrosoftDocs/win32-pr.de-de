---
title: ShowMessageAction.MessageBody-Eigenschaft
description: Für die Skripterstellung ruft den Meldungstext ab, der im Text des Meldungsfelds angezeigt wird, oder legt diesen fest.
ms.assetid: 7166e379-95f0-43f1-93a0-6a3d706dd627
keywords:
- MessageBody-Taskplaner
- MessageBody-Eigenschaft Taskplaner , ShowMessageAction-Objekt
- ShowMessageAction-Objekt Taskplaner , MessageBody-Eigenschaft
topic_type:
- apiref
api_name:
- ShowMessageAction.MessageBody
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5b408ad8642cc17b85d783a8f26d7de3322a26309897e4d9b3c128401449d0e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119139343"
---
# <a name="showmessageactionmessagebody-property"></a>ShowMessageAction.MessageBody-Eigenschaft

\[Dieses Objekt wird nicht mehr unterstützt. Sie können IExecAction mit der [**MsgBox Windows-Skriptfunktion**](/previous-versions/sfw6660x(v=vs.80)) verwenden, um eine Nachricht in der Benutzersitzung zu zeigen.\]

Für die Skripterstellung ruft den Meldungstext ab, der im Text des Meldungsfelds angezeigt wird, oder legt diesen fest.

## <a name="syntax"></a>Syntax


```VB
ShowMessageAction.MessageBody As String
```



## <a name="property-value"></a>Eigenschaftswert

Der Meldungstext, der im Text des Meldungsfelds angezeigt wird.

## <a name="remarks"></a>Hinweise

Parametrisierte Zeichenfolgen können im Meldungstext des Meldungsfelds verwendet werden. Weitere Informationen finden Sie im Abschnitt Beispiele in [**EventTrigger.ValueQueries**](eventtrigger-valuequeries.md).

Beim Festlegen dieses Eigenschaftswerts kann der Wert Text sein, der aus einer Ressourcendatei .dll wird. Eine spezialisierte Zeichenfolge wird verwendet, um auf den Text aus der Ressourcendatei zu verweisen. Das Format der Zeichenfolge ist $(@ Dll , ResourceID ), wobei DLL der Pfad zur .dll-Datei ist, die die Ressource enthält, und ResourceID der Bezeichner für den \[ \] \[ \] \[ \] \[ \] Ressourcentext ist. Wenn Sie diesen Eigenschaftswert beispielsweise auf $(@ %SystemRoot% System32ResourceName.dll, -101) festlegen, wird die -Eigenschaft auf den Wert des Ressourcentexts mit einem Bezeichner gleich \\ \\ -101 in der Datei %SystemRoot% \\ System32 \\ResourceName.dll festgelegt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                    |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                    |
| Ende des Supports (Server)<br/>    | Windows Server 2008 R2<br/>                                                       |
| Typbibliothek<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**ShowMessageAction**](showmessageaction.md)
</dt> </dl>

 

