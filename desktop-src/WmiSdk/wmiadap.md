---
description: Wmiadap ist eine Anwendung, die unter Windows ausgeführt wird und Leistungsinformationen im WMI-Repository aktualisieren kann.
ms.assetid: 459fe19e-3e2e-4a58-b3e7-75fd285f7389
ms.tgt_platform: multiple
title: wmiadap
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa5d2de65e8566283b341c5af52048cc79cc0299
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218472"
---
# <a name="wmiadap"></a>wmiadap

Wmiadap ist eine Anwendung, die unter Windows ausgeführt wird und Leistungsinformationen im WMI-Repository aktualisieren kann. Im Allgemeinen können Entwickler und IT-Administratoren Skripts erstellen, die auf Leistungsinformationen zugreifen, wie z. b. die Menge an Arbeitsspeicher, die von einer Anwendung verwendet wird. Im folgenden Thema wird die Befehlszeilenschnittstelle beschrieben, mit der Sie steuern können, wie wmiadap Informationen abruft.

Wmiadap wird mit dem Betriebssystem auf den meisten Systemen im Verzeichnis "C: \\ Windows \\ system32 \\ WBEM" installiert. Wenn Sie Fehlermeldungen zu wmiadap.exe sehen, suchen Sie [Microsoft-Support](https://support.microsoft.com/). Im Allgemeinen sollten Sie wmiadap.exe nicht von Ihrem System löschen, sofern nicht anders beschrieben.

Die Übertragung von Daten aus den Leistungs Bibliotheken und die Aktualisierung von Klassen, die von [**Win32 \_ perfrawdata**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) und [**Win32 \_ perfformatteddata**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) abgeleitet werden, erfolgt durch die Anbieter [wmiperfclass](wmi-providers.md) und [wmiperfinst](wmi-providers.md) . Der wmiperfclass-Anbieter aktualisiert die WMI- [Leistungs Objektklassen](/windows/desktop/CIMWin32Prov/performance-counter-classes) nur dann, wenn ein neues Leistungs Objekt hinzugefügt wird. Sie können wmiadap weiterhin mit dem Schalter **/r** ausführen, um die Windows-Treibermodell-Treiber zum Erstellen von Leistungs Objekten zu analysieren. Der Schalter **/f** erzwingt weiterhin ein Update der WMI-Klassen aus den Leistungs Bibliotheken.

Die folgenden Schalter sind an der Eingabeaufforderung verfügbar.

**wmiadap** \[  \] /f \[ **/r**\]

## <a name="switches"></a>Switches

<dl> <dt>

<span id="_f"></span><span id="_F"></span>**/f**
</dt> <dd>

Analysiert alle Leistungs Bibliotheken auf dem System und aktualisiert die von [**Win32 \_ perfrawdata**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) und [**Win32 \_ perfformatteddata**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata)abgeleiteten Klassen.

</dd> <dt>

<span id="_r"></span><span id="_R"></span>**/r**
</dt> <dd>

Analysiert alle Windows-Treibermodell Treiber auf dem System, um Leistungs Objekte zu erstellen.

</dd> </dl>

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Leistungs Bibliotheken und WMI](performance-libraries-and-wmi.md)
</dt> <dt>

[**WinMgmt**](winmgmt.md)
</dt> </dl>

 

 
