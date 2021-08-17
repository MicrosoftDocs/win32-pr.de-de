---
description: Die Aktivierungskontextfunktionen und -strukturen werden mit nebenseitigen Assemblys verwendet.
ms.assetid: b53b30e0-948e-406c-9fb4-9681dc3c5670
title: Referenz zum Aktivierungskontext
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72eb4bc136a95766a62bb96e67ac198f88fca905c60ba98e6bf922ce65a36389
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119142583"
---
# <a name="activation-context-reference"></a>Referenz zum Aktivierungskontext

Die Aktivierungskontextfunktionen und -strukturen werden mit nebenseitigen Assemblys verwendet.

In der folgenden Tabelle sind die Aktivierungskontextfunktionen aufgeführt.



| Funktion                                                   | Beschreibung                                                                                                                                             |
|------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ActivateActCtx**](/windows/desktop/api/Winbase/nf-winbase-activateactctx)                   | Aktiviert den angegebenen Aktivierungskontext.                                                                                                             |
| [**AddRefActCtx**](/windows/desktop/api/Winbase/nf-winbase-addrefactctx)                       | Erhöht den Verweiszähler des angegebenen Aktivierungskontexts.                                                                                     |
| [**CreateActCtx**](/windows/desktop/api/Winbase/nf-winbase-createactctxa)                       | Erstellt einen Aktivierungskontext.                                                                                                                          |
| [**DeactivateActCtx**](/windows/desktop/api/Winbase/nf-winbase-deactivateactctx)               | Deaktiviert den angegebenen Aktivierungskontext.                                                                                                           |
| [**FindActCtxSectionGuid**](/windows/desktop/api/Winbase/nf-winbase-findactctxsectionguid)     | Gibt In der [**ACTCTX \_ SECTION \_ KEYED \_ DATA-Struktur**](/windows/win32/api/winbase/ns-winbase-actctx_section_keyed_data) enthaltene Daten zurück, die der angegebenen GUID entsprechen.   |
| [**FindActCtxSectionString**](/windows/desktop/api/Winbase/nf-winbase-findactctxsectionstringa) | Gibt In der [**ACTCTX \_ SECTION \_ KEYED \_ DATA-Struktur**](/windows/win32/api/winbase/ns-winbase-actctx_section_keyed_data) enthaltene Daten zurück, die der angegebenen Zeichenfolge entsprechen. |
| [**GetCurrentActCtx**](/windows/desktop/api/Winbase/nf-winbase-getcurrentactctx)               | Gibt den aktuellen Aktivierungskontext zurück.                                                                                                                 |
| [**IsolationAwareCleanup**](/previous-versions/windows/desktop/legacy/aa375204(v=vs.85))     | Stellt sicher, dass Arbeitsspeicher freigegeben wird, wenn ein Manifest geladen, entladen und erneut geladen wird.                                                                         |
| [**QueryActCtxW**](/windows/desktop/api/Winbase/nf-winbase-queryactctxw)                       | Fragt den Aktivierungskontext nach Informationen zu einer Assembly oder Datei ab.                                                                               |
| [**QueryActCtxSettingsW**](/windows/desktop/api/Winbase/nf-winbase-queryactctxsettingsw)       | Gibt den Namespace und den Attributnamen des Attributs an, das abgefragt werden soll.                                                                      |
| [**ReleaseActCtx**](/windows/desktop/api/Winbase/nf-winbase-releaseactctx)                     | Dekrementisiert den Verweiszähler des angegebenen Aktivierungskontexts.                                                                                     |
| [**ZombifyActCtx**](/windows/desktop/api/Winbase/nf-winbase-zombifyactctx)                     | Deaktiviert den angegebenen Aktivierungskontext, gibt die Zuordnung jedoch nicht frei.                                                                               |



 

In der folgenden Tabelle sind die Aktivierungskontextstrukturen aufgeführt.



| Struktur                                                                                                        | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                  |
|------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_AUSFÜHRLICHE INFORMATIONEN ZUR AKTIVIERUNGSKONTEXTASSEMBLY \_ \_ \_**](/windows/desktop/api/Winnt/ns-winnt-activation_context_assembly_detailed_information) | Enthält ausführliche Informationen zum Aktivierungskontext.                                                                                                                                                                                                                                                                                                                                  |
| [**AUSFÜHRLICHE INFORMATIONEN ZUM \_ AKTIVIERUNGSKONTEXT \_ \_**](/windows/desktop/api/Winnt/ns-winnt-activation_context_detailed_information)                    | Enthält Informationen zur Assembly im Aktivierungskontext.                                                                                                                                                                                                                                                                                                                           |
| [**INDEX DER \_ AKTIVIERUNGSKONTEXTABFRAGE \_ \_**](/windows/desktop/api/Winnt/ns-winnt-activation_context_query_index)                                      | Enthält die Assembly im Aktivierungskontext und den Index der Datei in der Assembly.                                                                                                                                                                                                                                                                                           |
| [**ACTCTX**](/windows/win32/api/winbase/ns-winbase-actctxa)                                                                                     | Enthält Informationen, die einen bestimmten Aktivierungskontext beschreiben.                                                                                                                                                                                                                                                                                                                           |
| [**KEYED DATA IM \_ ACTCTX-ABSCHNITT \_ \_**](/windows/win32/api/winbase/ns-winbase-actctx_section_keyed_data)                                            | Gibt die Aktivierungskontextinformationen zusammen mit dem Aktivierungskontextabschnitt mit guid- oder 32-Bit-Ganzzahl-Tags zurück.                                                                                                                                                                                                                                                                   |
| [**\_ \_ ASSEMBLYDATEI – AUSFÜHRLICHE \_ INFORMATIONEN**](/windows/desktop/api/Winnt/ns-winnt-assembly_file_detailed_information)                              | Enthält Informationen zu einer Datei der Assembly im Aktivierungskontext.                                                                                                                                                                                                                                                                                                                 |
| [**\_INFORMATIONEN \_ ZUR AUSFÜHRUNGSEBENE DES \_ AKTIVIERUNGSKONTEXTS \_**](/windows/desktop/api/Winnt/ns-winnt-activation_context_run_level_information)                 | Wird von der [**QueryActCtxW-Funktion**](/windows/desktop/api/Winbase/nf-winbase-queryactctxw) verwendet.<br/> **Windows Server 2003 und Windows XP:** Diese Struktur ist nicht verfügbar.<br/>                                                                                                                                                                                                                                    |
| [**COMPATIBILITY \_ \_ CONTEXT-ELEMENT**](/windows/desktop/api/Winnt/ns-winnt-compatibility_context_element)                                         | Wird von der [**QueryActCtxW-Funktion**](/windows/desktop/api/Winbase/nf-winbase-queryactctxw) als Teil der [**ACTIVATION CONTEXT COMPATIBILITY \_ \_ \_ INFORMATION-Struktur**](/windows/desktop/api/Winnt/ns-winnt-activation_context_compatibility_information) verwendet. <br/> **Windows Server 2008 und früher und Windows Vista und früher:** Diese Struktur ist nicht verfügbar. Sie ist ab Windows Server 2008 R2 und Windows 7 verfügbar.<br/> |
| [**\_KOMPATIBILITÄTSINFORMATIONEN ZUM AKTIVIERUNGSKONTEXT \_ \_**](/windows/desktop/api/Winnt/ns-winnt-activation_context_compatibility_information)          | Wird von der [**QueryActCtxW-Funktion**](/windows/desktop/api/Winbase/nf-winbase-queryactctxw) verwendet.<br/> **Windows Server 2008 und früher und Windows Vista und früher:** Diese Struktur ist nicht verfügbar. Sie ist ab Windows Server 2008 R2 und Windows 7 verfügbar.<br/>                                                                                                                                   |



 

In der folgenden Tabelle sind die Aktivierungskontextenumerationen aufgeführt.

| Enumeration                                                                       | Beschreibung                                                                                                                                                                                                                                            |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ACTCTX– \_ ANGEFORDERTE \_ \_ AUSFÜHRUNGSEBENE**](/windows/desktop/api/Winnt/ne-winnt-actctx_requested_run_level)               | Beschreibt die angeforderte Ausführungsebene des Aktivierungskontexts. **Windows Server 2003 und Windows XP:** Diese Enumeration ist nicht verfügbar.<br/>                                                                                                      |
| [**ACTCTX \_ \_ COMPATIBILITY-ELEMENTTYP \_**](/windows/desktop/api/Winnt/ne-winnt-actctx_compatibility_element_type) | Beschreibt das Kompatibilitätselement im Anwendungsmanifest. **Windows Server 2008 und früher und Windows Vista und früher:** Diese Enumeration ist nicht verfügbar. Sie ist ab Windows Server 2008 R2 und Windows 7 verfügbar.<br/> |



 

 

