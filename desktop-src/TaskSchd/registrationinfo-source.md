---
title: RegistrationInfo. Source (Eigenschaft)
description: Ruft bei der Skripterstellung ab oder legt fest, wo die Aufgabe aus stammt. Beispielsweise kann eine Aufgabe aus einer Komponente, einem Dienst, einer Anwendung oder einem Benutzer stammen.
ms.assetid: b5bd987f-5c9f-4af0-99e2-aec92951f2be
keywords:
- Quell Eigenschaft Taskplaner
- Quell Eigenschaft Taskplaner, RegistrationInfo-Objekt
- RegistrationInfo-Objekt Taskplaner, Quell Eigenschaft
topic_type:
- apiref
api_name:
- RegistrationInfo.Source
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d360a20d1f0f4736db4dd6f136a579178a65ca70
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742441"
---
# <a name="registrationinfosource-property"></a>RegistrationInfo. Source (Eigenschaft)

Ruft bei der Skripterstellung ab oder legt fest, wo die Aufgabe aus stammt. Beispielsweise kann eine Aufgabe aus einer Komponente, einem Dienst, einer Anwendung oder einem Benutzer stammen.

## <a name="syntax"></a>Syntax


```VB
RegistrationInfo.Source As String
```



## <a name="property-value"></a>Eigenschaftswert

Der Ursprung der Aufgabe aus. Beispielsweise aus einer Komponente, einem Dienst, einer Anwendung oder einem Benutzer.

## <a name="remarks"></a>Bemerkungen

Beim Lesen oder Schreiben von XML für eine Aufgabe werden die Informationen zur Task Quelle mithilfe des [**Quell**](taskschedulerschema-source-registrationinfotype-element.md) Elements des Taskplaner Schemas angegeben.

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

 

 





