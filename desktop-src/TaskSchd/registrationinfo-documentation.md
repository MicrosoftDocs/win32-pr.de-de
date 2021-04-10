---
title: RegistrationInfo.Doc-Umschlag (Eigenschaft)
description: Ruft für die Skripterstellung eine beliebige zusätzliche Dokumentation für den Task ab oder legt diese fest.
ms.assetid: 12ce9461-0cc7-49d0-8c57-7ff3ca32850a
keywords:
- Dokumentations Eigenschaft Taskplaner
- Dokumentations Eigenschaft Taskplaner, RegistrationInfo-Objekt
- RegistrationInfo-Objekt Taskplaner, Dokumentations Eigenschaft
topic_type:
- apiref
api_name:
- RegistrationInfo.Documentation
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5832c78fae5c0ee9629077693db7e283369cc8af
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104102823"
---
# <a name="registrationinfodocumentation-property"></a>RegistrationInfo.Doc-Umschlag (Eigenschaft)

Ruft für die Skripterstellung eine beliebige zusätzliche Dokumentation für den Task ab oder legt diese fest.

## <a name="syntax"></a>Syntax


```VB
RegistrationInfo.Documentation As String
```



## <a name="property-value"></a>Eigenschaftswert

Jede zusätzliche Dokumentation, die der Aufgabe zugeordnet ist.

## <a name="remarks"></a>Bemerkungen

Beim Lesen oder Schreiben von XML für eine Aufgabe wird die zusätzliche Dokumentation für die Aufgabe mit dem [**Documentation**](taskschedulerschema-documentation-registrationinfotype-element.md) -Element des Taskplaner-Schemas angegeben.

Beim Festlegen dieses Eigenschafts Werts kann der Wert aus Text bestehen, der aus einer DLL-Datei der Ressource abgerufen wird. Eine spezialisierte Zeichenfolge wird verwendet, um auf den Text aus der Ressourcen Datei zu verweisen. Das Format der Zeichenfolge ist $ (@ \[ dll \] , \[ ResourceId \] ), wobei \[ dll \] der Pfad zur DLL-Datei, die die Ressource enthält, und \[ ResourceId der \] Bezeichner für den Ressourcen Text ist. Wenn z. b. der Wert dieser Eigenschaft auf $ (@% systemroot% \\ system32 \\ResourceName.dll,-101) festgelegt wird, wird die-Eigenschaft auf den Wert des Ressourcen Texts mit einem Bezeichner gleich-101 in der Datei% SystemRoot% \\ system32ResourceName.dll festgelegt \\ .

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                    |
| Typbibliothek<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> </dl>

 

 





