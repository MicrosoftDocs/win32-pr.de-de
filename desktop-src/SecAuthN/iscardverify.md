---
description: Stellt Dienste zum Festlegen des CHV-Codes (Card Holder Verification) und zum Überprüfen des Benutzers bereit.
ms.assetid: fa40c21c-1584-475e-89f6-f81f67e3b942
title: ISCardVerify-Schnittstelle
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardVerify
api_type:
- COM
api_location: ''
ms.openlocfilehash: e2f676360636395e0df811abed225c1a53be69a7da07f38a8acb08fc8d45e2ed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119141013"
---
# <a name="iscardverify-interface"></a>ISCardVerify-Schnittstelle

\[Die **ISCardVerify-Schnittstelle** ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt Anforderungen angegeben sind. Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die [Smartcardmodule](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten ähnliche Funktionen.\]

Die folgende Schnittstellendefinition wird als Standard bereitgestellt, der beim Entwickeln eines [](../secgloss/s-gly.md) [*Smartcard-Dienstanbieters*](../secgloss/c-gly.md)befolgt werden kann. Die **ISCardVerify-Schnittstelle** bietet Dienste zum Festlegen von CHV-Code (Card Holder Verification) und zum Überprüfen des Benutzers.

Die **ISCardVerify-Klasse** ist für Anwendungen definiert, die anwendungsspezifische CHV-Richtlinien implementieren und über detaillierte Kenntnisse der internen Implementierung der Smartcard verfügen.

Im Folgenden finden Sie eine typische Verwendung der **ISCardVerify-Schnittstelle.**

Im folgenden Verfahren wird **ISCardVerify** verwendet, um den CHV-Code zu ändern.

**So ändern Sie den CHV-Code einer Smartcard**

1.  Erstellen Sie eine **ISCardVerify-Schnittstelle** (über die entsprechende [**ISCardManage-Schnittstellenmethode).**](iscardmanage.md)
2.  Rufen Sie die [**ChangeCode-Methode auf,**](iscardverify-changecode.md) und geben Sie neuen Code an. Geben Sie dabei an, ob es sich um einen lokalen oder globalen Code handelt und ob er aktiviert oder deaktiviert ist.
3.  Geben Sie die **ISCardVerify-Schnittstelle** frei.

## <a name="members"></a>Member

Die **ISCardVerify-Schnittstelle** erbt von der [**IDispatch-Schnittstelle.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) **ISCardVerify** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ISCardVerify-Schnittstelle** verfügt über diese Methoden.



| Methode                                                        | Beschreibung                                                                                                                                 |
|:--------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------|
| [**ChangeCode**](iscardverify-changecode.md)                 | Ändert den aktuellen CHV-Code.<br/>                                                                                                    |
| [**ResetSecurityState**](iscardverify-resetsecuritystate.md) | Setzt den [*Sicherheitskontext*](../secgloss/s-gly.md) der Smartcard zurück.<br/> |
| [**Entsperren**](/previous-versions/windows/desktop/legacy/aa377269(v=vs.85))                       | Aktiviert den [*Sicherheitskontext*](../secgloss/s-gly.md)erneut.<br/>               |
| [**Überprüfung**](iscardverify-verify.md)                         | Authentifiziert den Benutzer.<br/>                                                                                                          |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur XP-Desktop-Apps\]<br/>          |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/> |
| Ende des Supports (Client)<br/>    | Windows XP<br/>                                |
| Ende des Supports (Server)<br/>    | Windows Server 2003<br/>                       |



 

 
