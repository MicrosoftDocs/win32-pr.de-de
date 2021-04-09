---
description: Die Aktivierungs Kontextfunktionen und-Strukturen werden mit parallelen Assemblys verwendet.
ms.assetid: b53b30e0-948e-406c-9fb4-9681dc3c5670
title: Aktivierungs Kontext Verweis
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d6f8225b4db8b22227edf2b779ed9e1b50da7a3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104042225"
---
# <a name="activation-context-reference"></a>Aktivierungs Kontext Verweis

Die Aktivierungs Kontextfunktionen und-Strukturen werden mit parallelen Assemblys verwendet.

In der folgenden Tabelle sind die Aktivierungs Kontextfunktionen aufgeführt.



| Funktion                                                   | BESCHREIBUNG                                                                                                                                             |
|------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Activateactctx**](/windows/desktop/api/Winbase/nf-winbase-activateactctx)                   | Aktiviert den angegebenen Aktivierungs Kontext.                                                                                                             |
| [**Adressfactctx**](/windows/desktop/api/Winbase/nf-winbase-addrefactctx)                       | Erhöht den Verweis Zähler für den angegebenen Aktivierungs Kontext.                                                                                     |
| [**"Kreateactctx"**](/windows/desktop/api/Winbase/nf-winbase-createactctxa)                       | Erstellt einen Aktivierungs Kontext.                                                                                                                          |
| [**Deactivateactctx**](/windows/desktop/api/Winbase/nf-winbase-deactivateactctx)               | Deaktiviert den angegebenen Aktivierungs Kontext.                                                                                                           |
| [**Findactctxsectionguid**](/windows/desktop/api/Winbase/nf-winbase-findactctxsectionguid)     | Gibt Daten zurück, die in der [**\_ \_ \_ Datenstruktur des ActCtx-Abschnitts**](/windows/win32/api/winbase/ns-winbase-actctx_section_keyed_data) enthalten sind, die der angegebenen GUID entspricht.   |
| [**Findactctxsectionstring**](/windows/desktop/api/Winbase/nf-winbase-findactctxsectionstringa) | Gibt Daten zurück, die in der [**\_ \_ \_ Datenstruktur des ActCtx-Abschnitts**](/windows/win32/api/winbase/ns-winbase-actctx_section_keyed_data) enthalten sind, die der angegebenen Zeichenfolge entspricht. |
| [**Getcurrentactctx**](/windows/desktop/api/Winbase/nf-winbase-getcurrentactctx)               | Gibt den aktuellen Aktivierungs Kontext zurück.                                                                                                                 |
| [**Isolationawarecleanup**](/previous-versions/windows/desktop/legacy/aa375204(v=vs.85))     | Stellt sicher, dass der Arbeitsspeicher freigegeben wird, wenn ein Manifest geladen, entladen und neu geladen wird.                                                                         |
| [**Queryactctxw**](/windows/desktop/api/Winbase/nf-winbase-queryactctxw)                       | Fragt den Aktivierungs Kontext nach Informationen zu einer Assembly oder Datei ab.                                                                               |
| [**Queryactctxsettingsw**](/windows/desktop/api/Winbase/nf-winbase-queryactctxsettingsw)       | Gibt den Namespace und den Attributnamen des Attributs an, das abgefragt werden soll.                                                                      |
| [**Releaseactctx**](/windows/desktop/api/Winbase/nf-winbase-releaseactctx)                     | Dekremente den Verweis Zähler für den angegebenen Aktivierungs Kontext.                                                                                     |
| [**Zombifyactctx**](/windows/desktop/api/Winbase/nf-winbase-zombifyactctx)                     | Deaktiviert den angegebenen Aktivierungs Kontext, hebt aber seine Freigabe nicht auf.                                                                               |



 

In der folgenden Tabelle sind die Aktivierungs Kontext Strukturen aufgeführt.



| Struktur                                                                                                        | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                  |
|------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_ \_ \_ ausführliche Informationen zur Aktivierungs Kontext Assembly \_**](/windows/desktop/api/Winnt/ns-winnt-activation_context_assembly_detailed_information) | Enthält ausführliche Informationen zum Aktivierungs Kontext.                                                                                                                                                                                                                                                                                                                                  |
| [**\_ \_ ausführliche \_ Informationen zum Aktivierungs Kontext**](/windows/desktop/api/Winnt/ns-winnt-activation_context_detailed_information)                    | Enthält Informationen über die Assembly im Aktivierungs Kontext.                                                                                                                                                                                                                                                                                                                           |
| [**\_ \_ Abfrage \_ Index für Aktivierungs Kontext**](/windows/desktop/api/Winnt/ns-winnt-activation_context_query_index)                                      | Enthält die Assembly im Aktivierungs Kontext und den Index der Datei in der Assembly.                                                                                                                                                                                                                                                                                           |
| [**ActCtx**](/windows/win32/api/winbase/ns-winbase-actctxa)                                                                                     | Enthält Informationen, die einen bestimmten Aktivierungs Kontext beschreiben.                                                                                                                                                                                                                                                                                                                           |
| [**verschlüsselte Daten des ActCtx- \_ Abschnitts \_ \_**](/windows/win32/api/winbase/ns-winbase-actctx_section_keyed_data)                                            | Gibt die Aktivierungs Kontextinformationen zusammen mit dem GUID-oder 32-Bit-Aktivierungs Kontext Abschnitt mit ganzzahligen Tags zurück.                                                                                                                                                                                                                                                                   |
| [**Ausführliche Informationen zur Assemblydatei \_ \_ \_**](/windows/desktop/api/Winnt/ns-winnt-assembly_file_detailed_information)                              | Enthält Informationen über eine Datei der Assembly im Aktivierungs Kontext.                                                                                                                                                                                                                                                                                                                 |
| [**Informationen zur Laufzeit auf dem Aktivierungs \_ Kontext \_ \_ \_**](/windows/desktop/api/Winnt/ns-winnt-activation_context_run_level_information)                 | Wird von der [**queryactctxw**](/windows/desktop/api/Winbase/nf-winbase-queryactctxw) -Funktion verwendet.<br/> **Windows Server 2003 und Windows XP:** Diese Struktur ist nicht verfügbar.<br/>                                                                                                                                                                                                                                    |
| [**Kompatibilitäts \_ Kontext \_ Element**](/windows/desktop/api/Winnt/ns-winnt-compatibility_context_element)                                         | Wird von der [**queryactctxw**](/windows/desktop/api/Winbase/nf-winbase-queryactctxw) -Funktion als Teil der [**Aktivierungs \_ Kontext- \_ Kompatibilitäts \_ Informations**](/windows/desktop/api/Winnt/ns-winnt-activation_context_compatibility_information) Struktur verwendet. <br/> **Windows Server 2008 und früher sowie Windows Vista und früher:** Diese Struktur ist nicht verfügbar. Sie steht ab Windows Server 2008 R2 und Windows 7 zur Verfügung.<br/> |
| [**\_ \_ Kompatibilitätsinformationen zum Aktivierungs Kontext \_**](/windows/desktop/api/Winnt/ns-winnt-activation_context_compatibility_information)          | Wird von der [**queryactctxw**](/windows/desktop/api/Winbase/nf-winbase-queryactctxw) -Funktion verwendet.<br/> **Windows Server 2008 und früher sowie Windows Vista und früher:** Diese Struktur ist nicht verfügbar. Sie steht ab Windows Server 2008 R2 und Windows 7 zur Verfügung.<br/>                                                                                                                                   |



 

In der folgenden Tabelle werden Aktivierungs Kontext Enumerationen aufgelistet.

| Enumeration                                                                       | Beschreibung                                                                                                                                                                                                                                            |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**von ActCtx \_ angeforderte \_ Testlauf- \_ Ebene**](/windows/desktop/api/Winnt/ne-winnt-actctx_requested_run_level)               | Beschreibt die angeforderte Lauf Ebene des Aktivierungs Kontexts. **Windows Server 2003 und Windows XP:** Diese Enumeration ist nicht verfügbar.<br/>                                                                                                      |
| [**ActCtx- \_ Kompatibilitäts \_ \_ Elementtyp**](/windows/desktop/api/Winnt/ne-winnt-actctx_compatibility_element_type) | Beschreibt das Kompatibilitäts Element im Anwendungs Manifest. **Windows Server 2008 und früher sowie Windows Vista und früher:** Diese Enumeration ist nicht verfügbar. Sie steht ab Windows Server 2008 R2 und Windows 7 zur Verfügung.<br/> |



 

 

