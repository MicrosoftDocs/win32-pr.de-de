---
description: Macht Methoden verfügbar, die zum Initialisieren einer zuletzt verwendeten (MRU-) Liste für ein Objekt für die automatische Vervollständigung verwendet werden.
title: Iaclcustommru-Schnittstelle
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IACLCustomMRU
api_type:
- COM
api_location: ''
ms.assetid: 6ebf64da-9eba-4ea7-91aa-242474097be1
ms.openlocfilehash: 54cda8d6cc3c7f1c46d6bce7736160b0da67a4c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104994623"
---
# <a name="iaclcustommru-interface"></a>Iaclcustommru-Schnittstelle

Macht Methoden verfügbar, die zum Initialisieren einer zuletzt verwendeten (MRU-) Liste für ein Objekt für die automatische Vervollständigung verwendet werden.

## <a name="members"></a>Member

Die **iaclcustommru** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **Iaclcustommru** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **iaclcustommru** -Schnittstelle verfügt über diese Methoden.



| Methode                                             | BESCHREIBUNG                                                             |
|:---------------------------------------------------|:------------------------------------------------------------------------|
| [**Addmrustring**](iaclcustommru-addmrustring.md) | Fügt der MRU-Liste einen Eintrag hinzu.<br/>                               |
| [**Initialisieren**](iaclcustommru-initialize.md)     | Lädt eine Liste von Zeichen folgen aus der Registrierung in die MRU-Liste.<br/> |



 

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>          |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/> |



 

 
