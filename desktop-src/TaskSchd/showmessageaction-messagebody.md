---
title: Showmessageaction. MessageBody-Eigenschaft
description: Ruft bei der Skripterstellung den Nachrichtentext ab, der im Textkörper des Meldungs Felds angezeigt wird, oder legt diesen fest.
ms.assetid: 7166e379-95f0-43f1-93a0-6a3d706dd627
keywords:
- MessageBody-Eigenschaft Taskplaner
- MessageBody-Eigenschaft Taskplaner, showmessageaction-Objekt
- Showmessageaction-Objekt Taskplaner, MessageBody-Eigenschaft
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
ms.openlocfilehash: a1604367a8daad1ae1b5f44c6021d22bf1aa7c5a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858738"
---
# <a name="showmessageactionmessagebody-property"></a>Showmessageaction. MessageBody-Eigenschaft

\[Dieses Objekt wird nicht mehr unterstützt. Sie können IExecAction mit der Windows Scripting [**MsgBox-Funktion**](/previous-versions/sfw6660x(v=vs.80)) verwenden, um eine Meldung in der Benutzersitzung anzuzeigen.\]

Ruft bei der Skripterstellung den Nachrichtentext ab, der im Textkörper des Meldungs Felds angezeigt wird, oder legt diesen fest.

## <a name="syntax"></a>Syntax


```VB
ShowMessageAction.MessageBody As String
```



## <a name="property-value"></a>Eigenschaftswert

Der Meldungs Text, der im Textkörper des Meldungs Felds angezeigt wird.

## <a name="remarks"></a>Bemerkungen

Parametrisierte Zeichen folgen können im Nachrichtentext des Meldungs Felds verwendet werden. Weitere Informationen finden Sie im Abschnitt "Beispiele" in " [**EventTrigger. valuequeries**](eventtrigger-valuequeries.md)".

Beim Festlegen dieses Eigenschafts Werts kann der Wert aus Text bestehen, der aus einer DLL-Datei der Ressource abgerufen wird. Eine spezialisierte Zeichenfolge wird verwendet, um auf den Text aus der Ressourcen Datei zu verweisen. Das Format der Zeichenfolge ist $ (@ \[ dll \] , \[ ResourceId \] ), wobei \[ dll \] der Pfad zur DLL-Datei, die die Ressource enthält, und \[ ResourceId der \] Bezeichner für den Ressourcen Text ist. Wenn z. b. der Wert dieser Eigenschaft auf $ (@% systemroot% \\ system32 \\ResourceName.dll,-101) festgelegt wird, wird die-Eigenschaft auf den Wert des Ressourcen Texts mit einem Bezeichner gleich-101 in der Datei% SystemRoot% \\ system32ResourceName.dll festgelegt \\ .

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                    |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                    |
| Ende des Supports (Server)<br/>    | Windows Server 2008 R2<br/>                                                       |
| Typbibliothek<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Showmessageaction**](showmessageaction.md)
</dt> </dl>

 

