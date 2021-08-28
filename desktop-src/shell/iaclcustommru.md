---
description: Macht Methoden verfügbar, die verwendet werden, um eine zuletzt verwendete Liste (MRU) für ein AutoVervollständigen-Objekt zu initialisieren.
title: IACLCustomMRU-Schnittstelle
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
ms.openlocfilehash: c4130ead959c326da55d2c02726c9db89ce363b616ea34cbfa545d179d1ee139
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119937040"
---
# <a name="iaclcustommru-interface"></a>IACLCustomMRU-Schnittstelle

Macht Methoden verfügbar, die verwendet werden, um eine zuletzt verwendete Liste (MRU) für ein AutoVervollständigen-Objekt zu initialisieren.

## <a name="members"></a>Member

Die **IACLCustomMRU-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IACLCustomMRU** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **IACLCustomMRU-Schnittstelle** verfügt über diese Methoden.



| Methode                                             | BESCHREIBUNG                                                             |
|:---------------------------------------------------|:------------------------------------------------------------------------|
| [**AddMRUString**](iaclcustommru-addmrustring.md) | Fügt der MRU-Liste einen Eintrag hinzu.<br/>                               |
| [**Initialisieren**](iaclcustommru-initialize.md)     | Lädt eine Liste von Zeichenfolgen aus der Registrierung in die MRU-Liste.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur XP-Desktop-Apps\]<br/>          |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/> |



 

 
