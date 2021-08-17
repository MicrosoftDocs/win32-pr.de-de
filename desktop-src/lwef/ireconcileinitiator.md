---
title: IReconcileInitiator-Schnittstelle
description: Macht Methoden verfügbar, die die Abstimmung von Kleinbuchstaben mit der Möglichkeit bereitstellen, den Initiator über seinen Fortschritt zu benachrichtigen, ein Beendigungsobjekt festzulegen und eine bestimmte Version eines Dokuments anzufordern. Der Initiator ist für die Implementierung dieser Schnittstelle verantwortlich.
ms.assetid: 1a32d67f-1ddc-49dc-af88-b8c41a50ac54
keywords:
- IReconcileInitiator-Schnittstelle – Legacy-Windows-Umgebungsfeatures
- IReconcileInitiator-Schnittstelle Legacy Windows Umgebungsfeatures , beschrieben
topic_type:
- apiref
api_name:
- IReconcileInitiator
api_location:
- Shell32.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff81862e5ff0b27b75f952749957e6559306257240f2a02aca5f34e3efc870cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118749140"
---
# <a name="ireconcileinitiator-interface"></a>IReconcileInitiator-Schnittstelle

Macht Methoden verfügbar, die die Abstimmung von Kleinbuchstaben mit der Möglichkeit bereitstellen, den Initiator über seinen Fortschritt zu benachrichtigen, ein Beendigungsobjekt festzulegen und eine bestimmte Version eines Dokuments anzufordern. Der Initiator ist für die Implementierung dieser Schnittstelle verantwortlich.

## <a name="members"></a>Member

Die **IReconcileInitiator-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IReconcileInitiator** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **IReconcileInitiator-Schnittstelle** verfügt über diese Methoden.



| Methode                                                                 | BESCHREIBUNG                                                                                                                                                                                                                                                                                                             |
|:-----------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SetAbortCallback**](/windows/win32/api/reconcil/nf-reconcil-ireconcileinitiator-setabortcallback)       | Legt das Objekt fest, über das der Initiator eine Abstimmung asynchron beenden kann. Ein Briefkastenabstimmungs-Objekt legt dieses Objekt in der Regel für Abstimmungen fest, die lang sind oder eine Benutzerinteraktion beinhalten. <br/>                                                                                              |
| [**SetProgressFeedback**](/windows/win32/api/reconcil/nf-reconcil-ireconcileinitiator-setprogressfeedback) | Gibt den Fortschritt an, den der Briefkasten-Abstimmungsschritt beim Abschließen des Abgleichs erzielt hat. Der Betrag ist ein Bruchteil und wird als Quotient der *UlProgress-* und *ulProgressMax-Parameter* berechnet. Abstimmungen sollten diese Methode in regelmäßigen Abständen während ihres Abstimmungsprozesses aufrufen. <br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur XP-Desktop-Apps\]<br/>                                                                   |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shell32.dll (Version 4.0 oder höher)</dt> </dl> |



 

