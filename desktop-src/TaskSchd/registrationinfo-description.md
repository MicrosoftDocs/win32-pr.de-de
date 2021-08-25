---
title: RegistrationInfo.Description (Eigenschaft)
description: Für die Skripterstellung ruft die Beschreibung der Aufgabe ab oder legt sie fest.
ms.assetid: bb85fa09-155c-452b-bf6e-28ac4f60cc42
keywords:
- Beschreibungseigenschaft Taskplaner
- Description-Eigenschaft Taskplaner , RegistrationInfo-Objekt
- RegistrationInfo-Taskplaner , Description-Eigenschaft
topic_type:
- apiref
api_name:
- RegistrationInfo.Description
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea6f141eddc40b21f1cf49e490fe30df5844e6029f821d9811b0e62ea55fa8ec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119872460"
---
# <a name="registrationinfodescription-property"></a>RegistrationInfo.Description (Eigenschaft)

Für die Skripterstellung ruft die Beschreibung der Aufgabe ab oder legt sie fest.

## <a name="syntax"></a>Syntax


```VB
RegistrationInfo.Description As String
```



## <a name="property-value"></a>Eigenschaftswert

Die Beschreibung des Tasks.

## <a name="remarks"></a>Hinweise

Beim Lesen oder Schreiben von XML für eine Aufgabe wird die Beschreibung der Aufgabe mithilfe des [**Description-Elements**](taskschedulerschema-description-registrationinfotype-element.md) des Taskplaner angegeben.

Beim Festlegen dieses Eigenschaftswerts kann der Wert Text sein, der aus einer Ressourcendatei .dll wird. Eine spezialisierte Zeichenfolge wird verwendet, um auf den Text aus der Ressourcendatei zu verweisen. Das Format der Zeichenfolge ist $(@ Dll , ResourceID ), wobei DLL der Pfad zur .dll-Datei ist, die die Ressource enthält, und ResourceID der Bezeichner für den \[ \] \[ \] \[ \] \[ \] Ressourcentext ist. Wenn Sie diesen Eigenschaftswert beispielsweise auf $(@ %SystemRoot% System32ResourceName.dll, -101) festlegen, wird die -Eigenschaft auf den Wert des Ressourcentexts mit einem Bezeichner gleich \\ \\ -101 in der Datei %SystemRoot% \\ System32 \\ResourceName.dll festgelegt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                    |
| Typbibliothek<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> </dl>

 

 





