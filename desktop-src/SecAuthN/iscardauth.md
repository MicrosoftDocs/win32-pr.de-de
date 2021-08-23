---
description: Die ISCardAuth-Schnittstellendefinition wird als Standard bereitgestellt, der bei der Entwicklung eines Smartcard-Dienstanbieters befolgt werden kann. Die ISCardAuth-Schnittstelle kann verwendet werden, um Authentifizierungsdienste verfügbar zu machen, die von einer Smartcard unterstützt werden.
ms.assetid: 6b8a5b90-49ad-48fd-813c-c3c3337ec8f1
title: ISCardAuth-Schnittstelle
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
ms.openlocfilehash: 55f92b06fb9c86c46ee0f9bf08350510ba4e6f897a95294a15265df7918de516
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119577850"
---
# <a name="iscardauth-interface"></a>ISCardAuth-Schnittstelle

\[Die **ISCardAuth-Schnittstelle** ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt Anforderungen angegeben sind. Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die [Smartcardmodule](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten ähnliche Funktionen.\]

Die **ISCardAuth-Schnittstellendefinition** wird als Standard bereitgestellt, der bei der Entwicklung eines [*Smartcard-Dienstanbieters*](../secgloss/s-gly.md) [*befolgt werden kann.*](../secgloss/c-gly.md)

Die **ISCardAuth-Schnittstelle** kann verwendet werden, um Authentifizierungsdienste verfügbar zu machen, die von einer Smartcard unterstützt werden. Zu diesen Diensten gehören Anwendungsauthentifizierung, Smartcardauthentifizierung und Benutzerauthentifizierung.

Das folgende Beispiel zeigt eine typische Verwendung der **ISCardAuth-Schnittstelle.**

**So verwenden Sie ISCardAuth**

1.  Erstellen Sie **eine ISCardAuth-Schnittstelle** (über die entsprechende [**ISCardManage-Schnittstellenmethode).**](iscardmanage.md)
2.  Rufen Sie die entsprechende **ISCardAuth-Methode** auf [**\_ (APP-Authentifizierung,**](iscardauth-app-auth.md) [**GetChallenge,**](iscardauth-getchallenge.md) [**\_ PIC-Authentifizierung**](iscardauth-icc-auth.md)oder [**\_ Benutzerauthentifizierung).**](iscardauth-user-auth.md)
3.  Geben Sie die **ISCardAuth-Schnittstelle** frei.

## <a name="members"></a>Member

Die **ISCardAuth-Schnittstelle** erbt von der [**IDispatch-Schnittstelle.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) **ISCardAuth** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ISCardAuth-Schnittstelle** verfügt über diese Methoden.



| Methode                                          | Beschreibung                                                                                    |
|:------------------------------------------------|:-----------------------------------------------------------------------------------------------|
| [**\_APP-Authentifizierung**](iscardauth-app-auth.md)        | Ermöglicht der Anwendung, sich mithilfe eines Challenge/Signature-Protokolls selbst zu authentifizieren.<br/> |
| [**GetChallenge**](iscardauth-getchallenge.md) | Gibt eine Herausforderung von der Smartcard zurück.<br/>                                            |
| [**\_ICC-Authentifizierung**](iscardauth-icc-auth.md)        | Ermöglicht einer Anwendung die Authentifizierung der Smartcard.<br/>                               |
| [**\_Benutzerauthentifizierung**](iscardauth-user-auth.md)      | Ermöglicht den Zugriff auf Benutzerauthentifizierungsdienste.<br/>                                      |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ XP-Desktop-Apps\]<br/>          |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/> |
| Ende des Supports (Client)<br/>    | Windows XP<br/>                                |
| Ende des Supports (Server)<br/>    | Windows Server 2003<br/>                       |



 

 
