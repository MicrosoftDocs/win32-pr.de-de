---
description: Bietet Dienste zum Festlegen von Code für die Überprüfung von CHV (Karteninhaber) und zum Überprüfen des Benutzers.
ms.assetid: fa40c21c-1584-475e-89f6-f81f67e3b942
title: Iscardverify-Schnittstelle
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
ms.openlocfilehash: f929028f96faaab6ddb03538e854db01196ae180
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757015"
---
# <a name="iscardverify-interface"></a>Iscardverify-Schnittstelle

\[Die **iscardverify** -Schnittstelle ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]

Die folgende Schnittstellen Definition wird als Standard bereitgestellt, der bei der Entwicklung eines [*Smartcard*](../secgloss/s-gly.md) - [*Dienstanbieters*](../secgloss/c-gly.md)befolgt werden kann. Die **iscardverify** -Schnittstelle bietet Dienste zum Festlegen von Code für die Überprüfung von CHV (Karteninhaber) und zum Überprüfen des Benutzers.

Die **iscardverify** -Klasse ist für Anwendungen definiert, die anwendungsspezifische CHV-Richtlinien implementieren, und die über ein detailliertes Wissen zur internen Implementierung der Smartcard verfügen.

Im folgenden finden Sie eine typische Verwendung der **iscardverify** -Schnittstelle.

Im folgenden Verfahren wird **iscardverify** verwendet, um den CHV-Code zu ändern.

**So ändern Sie den CHV-Code einer Smartcard**

1.  Erstellen Sie eine **iscardverify** -Schnittstelle (über die entsprechende [**iscardmanage**](iscardmanage.md) -Schnittstellen Methode).
2.  Nennen Sie die [**ChangeCode**](iscardverify-changecode.md) -Methode, und stellen Sie neuen Code bereit, um anzugeben, ob es sich um eine lokale oder globale Methode handelt und ob Sie aktiviert oder deaktiviert
3.  Geben Sie die **iscardverify** -Schnittstelle frei.

## <a name="members"></a>Member

Die **iscardverify** -Schnittstelle erbt von der [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstelle. **Iscardverify** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **iscardverify** -Schnittstelle verfügt über diese Methoden.



| Methode                                                        | BESCHREIBUNG                                                                                                                                 |
|:--------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------|
| [**ChangeCode**](iscardverify-changecode.md)                 | Ändert den aktuellen CHV-Code.<br/>                                                                                                    |
| [**Resetsecuritystate**](iscardverify-resetsecuritystate.md) | Setzt den [*Sicherheitskontext*](../secgloss/s-gly.md) der Smartcard zurück.<br/> |
| [**Blockierung**](/previous-versions/windows/desktop/legacy/aa377269(v=vs.85))                       | Aktiviert den [*Sicherheitskontext*](../secgloss/s-gly.md)erneut.<br/>               |
| [**Weisen**](iscardverify-verify.md)                         | Authentifiziert den Benutzer.<br/>                                                                                                          |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>          |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/> |
| Ende des Supports (Client)<br/>    | Windows XP<br/>                                |
| Ende des Supports (Server)<br/>    | Windows Server 2003<br/>                       |



 

 
