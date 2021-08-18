---
description: Die ComponentRequestState-Eigenschaft des Session-Objekts ruft eine Änderung des Aktionszustands einer Zeile in der Component-Tabelle ab oder fordert eine Änderung an.
ms.assetid: d0b50c25-dca6-4bdf-8ee9-490e436fcc5b
title: Session.ComponentRequestState-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.ComponentRequestState
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 3cef17ab3a4781f925e92968bd50dfedddd9a0df8e1781a2f209712fc447ef10
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118625236"
---
# <a name="sessioncomponentrequeststate-property"></a>Session.ComponentRequestState-Eigenschaft

Die **ComponentRequestState-Eigenschaft** des [**Session-Objekts**](session-object.md) ruft eine Änderung des Aktionszustands einer Zeile in der [Component-Tabelle](component-table.md)ab oder fordert eine Änderung an.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```JScript
propVal = Session.ComponentRequestState
```



## <a name="property-value"></a>Eigenschaftswert

Erforderlicher Zeichenfolgenname des Komponentenelements, Primärschlüssel der Komponententabelle.

## <a name="remarks"></a>Hinweise



| Auswahlzustand        | Wert | Beschreibung                                                    |
|------------------------|-------|----------------------------------------------------------------|
| Null                   | Null  | Fordert an, dass für dieses Element keine Aktion ausgeführt wird.                |
| msiInstallStateAbsent  | 2     | Das Element muss entfernt werden.                                         |
| msiInstallStateLocal   | 3     | Das Element muss lokal installiert werden.                               |
| msiInstallStateSource  | 4     | Das Element muss auf dem Quellmedium installiert und ausgeführt werden.         |
| msiInstallStateDefault | 5     | Wenn das Element installiert ist, muss es im gleichen Zustand neu installiert werden. |



 

Wenn die Eigenschaft fehlschlägt, können Sie erweiterte Fehlerinformationen mithilfe der [**LastErrorRecord-Methode**](installer-lasterrorrecord.md) abrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installationsprogramm 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installationsprogramm auf Windows Server 2003 oder Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ ISession ist als 000C109E-0000-0000-C000-0000000000046 definiert.<br/>                                                                                                                                                                             |



 

 




