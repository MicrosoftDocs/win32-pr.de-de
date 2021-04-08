---
description: Enumerationen, die in der Dateiverwaltung verwendet werden.
ms.assetid: 14b1cfff-5e47-4309-8e62-fb5c8da9ce97
title: Dateiverwaltungs-Enumerationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7b53d8f53bf9dbe16c15d21171e52ea3dd0015d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960649"
---
# <a name="file-management-enumerations"></a>Dateiverwaltungs-Enumerationen

Die folgenden Enumerationen werden in der Dateiverwaltung verwendet.

## <a name="in-this-section"></a>In diesem Abschnitt



| Enumeration                                                                   | Beschreibung                                                                                                                                                                                                                                 |
|-------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**COPYFILE2- \_ Kopier \_ Phase**](/windows/desktop/api/WinBase/ne-winbase-copyfile2_copy_phase)<br/>             | Gibt die Phase einer Kopie zum Zeitpunkt eines Fehlers an.<br/>                                                                                                                                                                           |
| [**COPYFILE2- \_ Nachrichten \_ Aktion**](/windows/desktop/api/WinBase/ne-winbase-copyfile2_message_action)<br/>     | Wird von der [*CopyFile2ProgressRoutine*](/windows/desktop/api/WinBase/nc-winbase-pcopyfile2_progress_routine) -Rückruffunktion zurückgegeben, um anzugeben, welche Aktion für den ausstehenden Kopiervorgang ausgeführt werden soll.<br/>                                                             |
| [**COPYFILE2 \_ - \_ Nachrichtentyp**](/windows/desktop/api/WinBase/ne-winbase-copyfile2_message_type)<br/>         | Gibt den Nachrichtentyp an, der in der [**COPYFILE2- \_ Nachrichten**](/windows/desktop/api/WinBase/ns-winbase-copyfile2_message) Struktur an die [*CopyFile2ProgressRoutine*](/windows/desktop/api/WinBase/nc-winbase-pcopyfile2_progress_routine) -Rückruffunktion übertragen wird.<br/>                                       |
| [**CSV- \_ Steuerelement \_ op**](/windows/desktop/api/WinIoCtl/ne-winioctl-csv_control_op)<br/>                         | Gibt den Typ des CSV-Steuerelement Vorgangs an, der mit dem [**FSCTL- \_ CSV- \_ Steuer**](/windows/win32/api/winioctl/ni-winioctl-fsctl_csv_control) Element Code verwendet werden soll.<br/>                                                                                                       |
| [**Datei- \_ ID- \_ Typ**](/windows/desktop/api/WinBase/ne-winbase-file_id_type)<br/>                             | Diskriminator für die Union in der [**Datei- \_ ID- \_ deskriptorstruktur**](/windows/desktop/api/WinBase/ns-winbase-file_id_descriptor) .<br/>                                                                                                                                 |
| [**Datei \_ Informationen \_ nach \_ handle- \_ Klasse**](/windows/win32/api/minwinbase/ne-minwinbase-file_info_by_handle_class)<br/> | Identifiziert den Typ der Dateiinformationen, die [**getfileinformationbyshandex**](/windows/desktop/api/WinBase/nf-winbase-getfileinformationbyhandleex) abrufen soll, oder [**setfileinformationbyhandle**](/windows/desktop/api/FileAPI/nf-fileapi-setfileinformationbyhandle) muss festgelegt werden.<br/>                |
| [**findex- \_ Informations \_ Ebenen**](/windows/win32/api/minwinbase/ne-minwinbase-findex_info_levels)<br/>             | Definiert Werte, die mit der [**findfirstfileex**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfileexa) -Funktion verwendet werden, um die Informationsebene der zurückgegebenen Daten anzugeben.<br/>                                                                                 |
| [**findex- \_ Suchvorgänge \_**](/windows/win32/api/minwinbase/ne-minwinbase-findex_search_ops)<br/>               | Definiert Werte, die mit der [**findfirstfileex**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfileexa) -Funktion verwendet werden, um den auszuführenden Filtertyp anzugeben.<br/>                                                                                           |
| [**\_fileex- \_ Informations \_ Ebenen erhalten**](/windows/win32/api/minwinbase/ne-minwinbase-get_fileex_info_levels)<br/>        | Definiert Werte, die mit den Funktionen [**getfileattributesex**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesexa) und [**getfileattributestransagiert**](/windows/desktop/api/WinBase/nf-winbase-getfileattributestransacteda) verwendet werden, um die Informationsebene der zurückgegebenen Daten anzugeben.<br/> |
| [**Prioritäts \_ Hinweis**](/windows/desktop/api/WinBase/ne-winbase-priority_hint)<br/>                            | Definiert Werte, die mit der Datei-e/a- [**\_ \_ Prioritäts \_ Hinweis \_ Informations**](/windows/desktop/api/WinBase/ns-winbase-file_io_priority_hint_info) Struktur verwendet werden, um den Prioritäts Hinweis für einen Datei-e/a-Vorgang anzugeben<br/>                                                      |
| [**Stream- \_ Informations \_ Ebenen**](/windows/desktop/api/fileapi/ne-fileapi-stream_info_levels)<br/>                 | Definiert Werte, die mit der [**findfirststreamw**](/windows/desktop/api/fileapi/nf-fileapi-findfirststreamw) -Funktion verwendet werden, um die Informationsebene der zurückgegebenen Daten anzugeben.<br/>                                                                               |



 

 

