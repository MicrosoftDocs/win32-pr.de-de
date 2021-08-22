---
title: RegistrationInfo.Author-Eigenschaft
description: Ruft für die Skripterstellung den Ersteller der Aufgabe ab oder legt diese fest.
ms.assetid: ba355a3b-cda3-4d4f-8504-f77f3d9eb21a
keywords:
- Taskplaner der Erstellungseigenschaft
- Author-Eigenschaft Taskplaner , RegistrationInfo-Objekt
- RegistrationInfo-Objekt Taskplaner , Author-Eigenschaft
topic_type:
- apiref
api_name:
- RegistrationInfo.Author
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a136f41b27f69d95a0817efa24931a994237da90c6c2e0eaf581149687664f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118858854"
---
# <a name="registrationinfoauthor-property"></a>RegistrationInfo.Author-Eigenschaft

Ruft für die Skripterstellung den Ersteller der Aufgabe ab oder legt diese fest.

## <a name="syntax"></a>Syntax


```VB
RegistrationInfo.Author As String
```



## <a name="property-value"></a>Eigenschaftswert

Der Autor der Aufgabe.

## <a name="remarks"></a>Hinweise

Beim Lesen oder Schreiben von XML für eine Aufgabe wird der Taskautor mit dem [**Author-Element**](taskschedulerschema-author-registrationinfotype-element.md) des Taskplaner Schemas angegeben.

Beim Festlegen dieses Eigenschaftswerts kann der Wert Text sein, der aus einer Ressource .dll Datei abgerufen wird. Eine spezialisierte Zeichenfolge wird verwendet, um auf den Text aus der Ressourcendatei zu verweisen. Das Format der Zeichenfolge ist $(@ \[ Dll \] , \[ ResourceID ), wobei DLL \] der Pfad zu der .dll Datei mit der Ressource und \[ \] \[ ResourceID \] der Bezeichner für den Ressourcentext ist. Wenn Sie z. B. diesen Eigenschaftswert auf $(@ %SystemRoot% \\ System32 \\ResourceName.dll, -101) festlegen, wird die -Eigenschaft auf den Wert des Ressourcentexts mit einem Bezeichner festgelegt, der in der %SystemRoot% \\ System32ResourceName.dll-Datei gleich -101 \\ ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                    |
| Typbibliothek<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> </dl>

 

 





