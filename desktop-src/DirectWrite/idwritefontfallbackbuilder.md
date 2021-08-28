---
title: IDWriteFontFallbackBuilder-Schnittstelle
description: Ermöglicht ihnen das Erstellen von Unicode-Fallbackzuordnungen für Schriftarten und das Erstellen eines Schriftartfallbackobjekts aus diesen Zuordnungen.
ms.assetid: 462AC12E-C856-4D8F-83AF-FAC3221425C2
keywords:
- IDWriteFontFallbackBuilder-Schnittstelle Direct Write
- IDWriteFontFallbackBuilder-Schnittstelle Direct Write , beschrieben
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
ms.openlocfilehash: 3f42bc9882c238bb1167c76e941c4f183eef05e12d5d8dc70305b0c01e048797
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120051391"
---
# <a name="idwritefontfallbackbuilder-interface"></a>IDWriteFontFallbackBuilder-Schnittstelle

Ermöglicht ihnen das Erstellen von Unicode-Fallbackzuordnungen für Schriftarten und das Erstellen eines Schriftartfallbackobjekts aus diesen Zuordnungen.

## <a name="members"></a>Member

Die **IDWriteFontFallbackBuilder-Schnittstelle erbt** von der [**IUnknown-Schnittstelle.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IDWriteFontFallbackBuilder** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **IDWriteFontFallbackBuilder-Schnittstelle** verfügt über diese Methoden.



| Methode                                                                      | BESCHREIBUNG                                                                                  |
|:----------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------|
| [**HinzufügenMapping**](idwritefontfallbackbuilder-addmapping.md)                 | Fügt eine einzelne Zuordnung an die Liste an. Rufen Sie dies einmal für jede zusätzliche Zuordnung auf.<br/> |
| [**AddMappings**](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritefontfallbackbuilder-addmappings)               | Fügen Sie alle Zuordnungen aus einem vorhandenen Schriftartfallbackobjekt hinzu.<br/>                       |
| [**CreateFontFallback**](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritefontfallbackbuilder-createfontfallback) | Erstellt das endgültige Fallbackobjekt aus den hinzugefügten Zuordnungen.<br/>                    |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8.1 \|Desktop-Apps UWP-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 \[R2-Desktop-Apps \| UWP-Apps\]<br/>                          |
| Unterstützte Mindestversion (Telefon)<br/>  | Windows Phone 8.1 \[ Windows Phone Silverlight 8.1- und Windows Runtime-Apps\]<br/> |
| Bibliothek<br/>                  | <dl> <dt>Dwrite.lib</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>Dwrite.dll</dt> </dl>   |



 

