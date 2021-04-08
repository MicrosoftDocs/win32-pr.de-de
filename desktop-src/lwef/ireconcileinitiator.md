---
title: Ireconcileinitiator-Schnittstelle
description: Macht Methoden verfügbar, die die Aktentasche-Auflösung mit der Möglichkeit bereitstellen, den Initiator über den Fortschritt zu benachrichtigen, ein Beendigungs Objekt festzulegen und eine bestimmte Version eines Dokuments anzufordern. Der Initiator ist für die Implementierung dieser Schnittstelle verantwortlich.
ms.assetid: 1a32d67f-1ddc-49dc-af88-b8c41a50ac54
keywords:
- Ireconcileinitiator Interface Legacy Windows-Umgebungs Features
- Ireconcileinitiator Interface Legacy Windows-Umgebungs Features, beschrieben
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
ms.openlocfilehash: 759ad26fd87db7076811b9b31d6ef39df1479e3e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741600"
---
# <a name="ireconcileinitiator-interface"></a>Ireconcileinitiator-Schnittstelle

Macht Methoden verfügbar, die die Aktentasche-Auflösung mit der Möglichkeit bereitstellen, den Initiator über den Fortschritt zu benachrichtigen, ein Beendigungs Objekt festzulegen und eine bestimmte Version eines Dokuments anzufordern. Der Initiator ist für die Implementierung dieser Schnittstelle verantwortlich.

## <a name="members"></a>Member

Die **ireconcileinitiator** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **Ireconcileinitiator** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ireconcileinitiator** -Schnittstelle verfügt über diese Methoden.



| Methode                                                                 | BESCHREIBUNG                                                                                                                                                                                                                                                                                                             |
|:-----------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**"-Tabortcallback"**](/windows/win32/api/reconcil/nf-reconcil-ireconcileinitiator-setabortcallback)       | Legt das-Objekt fest, über das der Initiator eine Abstimmung asynchron beenden kann. Bei einer Aktentasche-Synchronisierung wird dieses Objekt in der Regel für reversationen festgelegt, die langwierig sind oder eine Benutzerinteraktion umfassen. <br/>                                                                                              |
| [**Setprogressfeedback**](/windows/win32/api/reconcil/nf-reconcil-ireconcileinitiator-setprogressfeedback) | Gibt den Fortschritt an, den der Aktentasche-Konflikt bei der ababstimmung durchgeführt hat. Der Betrag ist ein Bruchteil und wird als Quotienten der *ulprogress* -und *ulprogressmax* -Parameter berechnet. Die Abstimmung sollte diese Methode in regelmäßigen Abständen während Ihres Abstimmungs Vorgangs aufzurufen. <br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                                                   |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shell32.dll (Version 4,0 oder höher)</dt> </dl> |



 

