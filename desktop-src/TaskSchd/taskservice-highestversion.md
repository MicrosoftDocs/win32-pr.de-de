---
title: TaskService.HighestVersion-Eigenschaft
description: Gibt für die Skripterstellung die höchste Version von Taskplaner an, die ein Computer unterstützt.
ms.assetid: b4e55e46-6f33-4224-811b-06bf218dd1ac
keywords:
- HighestVersion-Eigenschaft Taskplaner
- HighestVersion-Eigenschaft Taskplaner , TaskService-Objekt
- TaskService-Objekt Taskplaner , HighestVersion-Eigenschaft
topic_type:
- apiref
api_name:
- TaskService.HighestVersion
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e27618490fcf404936532d272402bebc03d94eb72ba8156e897f344b708d90ec
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119959490"
---
# <a name="taskservicehighestversion-property"></a>TaskService.HighestVersion-Eigenschaft

Gibt für die Skripterstellung die höchste Version von Taskplaner an, die ein Computer unterstützt.

## <a name="syntax"></a>Syntax


```VB
TaskService.HighestVersion As Integer
```



## <a name="property-value"></a>Eigenschaftswert

Die höchste Version von Taskplaner, die ein Computer unterstützt. Die höchste Version ist ein Wert, der an der 16-Bit-Grenze in MajorVersion/MinorVersion unterteilt ist. Der Taskplaner-Dienst gibt 1 für die Hauptversion und 2 für die Nebenversion zurück. Verwenden Sie die [CLng-Funktion,](/previous-versions//ck4c5842(v=vs.85)) um den ganzzahligen Wert der Eigenschaft abzurufen.

## <a name="examples"></a>Beispiele

Der folgende Code zeigt, wie Sie die [CLng-Funktion](/previous-versions//ck4c5842(v=vs.85)) verwenden, um den Wert der **HighestVersion-Eigenschaft** abzurufen.


```VB
wscript.echo service.HighestVersion
Test = clng( service.HighestVersion )
If Test <> 65538  Then
    wscript.echo "Fail"

Else
    wscript.echo "Pass"
End If
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                    |
| Typbibliothek<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

