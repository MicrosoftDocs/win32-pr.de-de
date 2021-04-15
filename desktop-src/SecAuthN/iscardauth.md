---
description: Die iscardauth-Schnittstellen Definition wird als Standard bereitgestellt, der bei der Entwicklung eines Smartcard-Dienstanbieters befolgt werden kann. Die iscardauth-Schnittstelle kann verwendet werden, um von einer Smartcard unterstützte Authentifizierungsdienste verfügbar zu machen.
ms.assetid: 6b8a5b90-49ad-48fd-813c-c3c3337ec8f1
title: Iscardauth-Schnittstelle
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardAuth
api_type:
- COM
api_location: ''
ms.openlocfilehash: bf8df3702aceb2ac8bbf5ad090802be2dc07e45a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484723"
---
# <a name="iscardauth-interface"></a>Iscardauth-Schnittstelle

\[Die **iscardauth** -Schnittstelle ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]

Die **iscardauth** -Schnittstellen Definition wird als Standard bereitgestellt, der bei der Entwicklung eines [*Smartcard*](../secgloss/s-gly.md) - [*Dienstanbieters*](../secgloss/c-gly.md)befolgt werden kann.

Die **iscardauth** -Schnittstelle kann verwendet werden, um von einer Smartcard unterstützte Authentifizierungsdienste verfügbar zu machen. Zu diesen Diensten gehören die Anwendungs Authentifizierung, die Smartcard-Authentifizierung und die Benutzerauthentifizierung.

Das folgende Beispiel zeigt eine typische Verwendung der **iscardauth** -Schnittstelle.

**So verwenden Sie iscardauth**

1.  Erstellen Sie eine **iscardauth** -Schnittstelle (über die entsprechende [**iscardmanage**](iscardmanage.md) -Schnittstellen Methode).
2.  Aufrufen der entsprechenden **iscardauth** -Methode (app-Authentifizierung, [**getchallenge**](iscardauth-getchallenge.md), [**ICC \_**](iscardauth-icc-auth.md)-Authentifizierung oder [**Benutzer \_**](iscardauth-user-auth.md)Authentifizierung).[**\_**](iscardauth-app-auth.md)
3.  Geben Sie die **iscardauth** -Schnittstelle frei.

## <a name="members"></a>Member

Die **iscardauth** -Schnittstelle erbt von der [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstelle. **Iscardauth** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **iscardauth** -Schnittstelle verfügt über diese Methoden.



| Methode                                          | BESCHREIBUNG                                                                                    |
|:------------------------------------------------|:-----------------------------------------------------------------------------------------------|
| [**APP \_ -Authentifizierung**](iscardauth-app-auth.md)        | Ermöglicht es der Anwendung, sich mit einem Challenge/Signature-Protokoll zu authentifizieren.<br/> |
| [**Getchallenge**](iscardauth-getchallenge.md) | Gibt eine Herausforderung von der Smartcard zurück.<br/>                                            |
| [**ICC \_ -Authentifizierung**](iscardauth-icc-auth.md)        | Ermöglicht es einer Anwendung, die Smartcard zu authentifizieren.<br/>                               |
| [**Benutzer \_ Authentifizierung**](iscardauth-user-auth.md)      | Ermöglicht den Zugriff auf Benutzer Authentifizierungsdienste.<br/>                                      |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>          |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/> |
| Ende des Supports (Client)<br/>    | Windows XP<br/>                                |
| Ende des Supports (Server)<br/>    | Windows Server 2003<br/>                       |



 

 
