---
title: Idschreitefontfallbackbuilder-Schnittstelle
description: Ermöglicht das Erstellen von Unicode-Schriftart-Fall Back-Zuordnungen und das Erstellen eines Schriftart-Fall Back-Objekts aus diesen Zuordnungen.
ms.assetid: 462AC12E-C856-4D8F-83AF-FAC3221425C2
keywords:
- Idwrite-fontfallbackbuilder-Schnittstelle direkt schreiben
- Direkter Schreibvorgang für idschreitefontfallbackbuilder-Schnittstelle, beschrieben
topic_type:
- apiref
api_name:
- IDWriteFontFallbackBuilder
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38cd1770bdd9617f53bb48d725b55c466b12c263
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956704"
---
# <a name="idwritefontfallbackbuilder-interface"></a>Idschreitefontfallbackbuilder-Schnittstelle

Ermöglicht das Erstellen von Unicode-Schriftart-Fall Back-Zuordnungen und das Erstellen eines Schriftart-Fall Back-Objekts aus diesen Zuordnungen.

## <a name="members"></a>Member

Die **idschreitefontfallbackbuilder** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **Idschreitefontfallbackbuilder** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **idschreitefontfallbackbuilder** -Schnittstelle verfügt über diese Methoden.



| Methode                                                                      | BESCHREIBUNG                                                                                  |
|:----------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------|
| [**AddMapping**](idwritefontfallbackbuilder-addmapping.md)                 | Fügt eine einzelne Zuordnung an die Liste an. Dies wird einmal für jede weitere Zuordnung aufgerufen.<br/> |
| [**Addmappings**](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritefontfallbackbuilder-addmappings)               | Fügen Sie alle Zuordnungen von einem vorhandenen Schriftart Fall Back Objekt hinzu.<br/>                       |
| [**"Kreatefontfallback"**](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritefontfallbackbuilder-createfontfallback) | Erstellt das fertige Fall Back Objekt aus den hinzugefügten Zuordnungen.<br/>                    |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8.1 \[ Desktop-Apps \| UWP-apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 R2 \[ -Desktop-Apps \| UWP-apps\]<br/>                          |
| Unterstützte Mindestversion (Telefon)<br/>  | Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 und Windows-Runtime apps\]<br/> |
| Bibliothek<br/>                  | <dl> <dt>Dwrite. lib</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>Dwrite.dll</dt> </dl>   |



 

