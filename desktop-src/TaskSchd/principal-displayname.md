---
title: Principal. Display Name (Eigenschaft)
description: Ruft bei der Skripterstellung den Namen des Prinzipals ab oder legt ihn fest.
ms.assetid: 73caf263-f597-4bea-ae89-32f9919d7a70
keywords:
- Display Name-Eigenschaft Taskplaner
- Display Name-Eigenschaft Taskplaner, Prinzipal Objekt
- Principal Object Taskplaner, Display Name-Eigenschaft
topic_type:
- apiref
api_name:
- Principal.DisplayName
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31a76ec9473bccb20ec484259ab8adfe26ad6441
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741873"
---
# <a name="principaldisplayname-property"></a>Principal. Display Name (Eigenschaft)

Ruft bei der Skripterstellung den Namen des Prinzipals ab oder legt ihn fest.

## <a name="syntax"></a>Syntax


```VB
Principal.DisplayName As String
```



## <a name="property-value"></a>Eigenschaftswert

Der Name des Prinzipals.

## <a name="remarks"></a>Bemerkungen

Beim Lesen oder Schreiben von XML für eine Aufgabe wird der Anzeige Name für einen Prinzipal im [**Display Name**](taskschedulerschema-displayname-principaltype-element.md) -Element des Taskplaner-Schemas angegeben.

Beim Festlegen dieses Eigenschafts Werts kann der Wert aus Text bestehen, der aus einer DLL-Datei der Ressource abgerufen wird. Eine spezialisierte Zeichenfolge wird verwendet, um auf den Text aus der Ressourcen Datei zu verweisen. Das Format der Zeichenfolge ist $ (@ \[ dll \] , \[ ResourceId \] ), wobei \[ dll \] der Pfad zur DLL-Datei, die die Ressource enthält, und \[ ResourceId der \] Bezeichner für den Ressourcen Text ist. Wenn Sie diesen Eigenschafts Wert z. b. auf $ (@% systemroot% \\ system32 \\ResourceName.dll,-101) festlegen, wird die-Eigenschaft auf den Wert des Ressourcen Texts mit einem Bezeichner festgelegt, der in der Datei "% SystemRoot% System32ResourceName.dll" gleich-101 ist \\ \\ .

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
</dt> <dt>

[**Prinzipal**](principal.md)
</dt> </dl>

 

 





