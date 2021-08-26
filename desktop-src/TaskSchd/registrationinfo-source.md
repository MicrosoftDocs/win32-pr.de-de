---
title: RegistrationInfo.Source(Eigenschaft)
description: Für die Skripterstellung ruft ab oder legt fest, woher die Aufgabe stammt. Beispielsweise kann eine Aufgabe von einer Komponente, einem Dienst, einer Anwendung oder einem Benutzer stammen.
ms.assetid: b5bd987f-5c9f-4af0-99e2-aec92951f2be
keywords:
- Quelleigenschafts-Taskplaner
- Quelleigenschaft Taskplaner , RegistrationInfo-Objekt
- RegistrationInfo-Taskplaner , Source-Eigenschaft
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
ms.openlocfilehash: 97320d63823599e52327533afdba62f795622263e57878515ddd7ade9c98070b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120126030"
---
# <a name="registrationinfosource-property"></a>RegistrationInfo.Source(Eigenschaft)

Für die Skripterstellung ruft ab oder legt fest, woher die Aufgabe stammt. Beispielsweise kann eine Aufgabe von einer Komponente, einem Dienst, einer Anwendung oder einem Benutzer stammen.

## <a name="syntax"></a>Syntax


```VB
RegistrationInfo.Source As String
```



## <a name="property-value"></a>Eigenschaftswert

Woher die Aufgabe stammt. Beispielsweise aus einer Komponente, einem Dienst, einer Anwendung oder einem Benutzer.

## <a name="remarks"></a>Hinweise

Beim Lesen oder Schreiben von XML für einen Task werden die Informationen der Taskquelle mithilfe des [**Source-Elements**](taskschedulerschema-source-registrationinfotype-element.md) des Taskplaner angegeben.

Beim Festlegen dieses Eigenschaftswerts kann der Wert Text sein, der aus einer Ressourcendatei .dll wird. Eine spezialisierte Zeichenfolge wird verwendet, um auf den Text aus der Ressourcendatei zu verweisen. Das Format der Zeichenfolge ist $(@ Dll , ResourceID ), wobei DLL der Pfad zur .dll-Datei ist, die die Ressource enthält, und ResourceID der Bezeichner für den \[ \] \[ \] \[ \] \[ \] Ressourcentext ist. Wenn Sie diesen Eigenschaftswert beispielsweise auf $(@ %SystemRoot% System32ResourceName.dll, -101) festlegen, wird die -Eigenschaft auf den Wert des Ressourcentexts mit einem Bezeichner gleich \\ \\ -101 in der Datei %SystemRoot% \\ System32 \\ResourceName.dll festgelegt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                    |
| Typbibliothek<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> </dl>

 

 





