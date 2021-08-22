---
description: Wmiadap ist eine Anwendung, die auf einem Windows, die Leistungsinformationen im WMI-Repository aktualisieren kann.
ms.assetid: 459fe19e-3e2e-4a58-b3e7-75fd285f7389
ms.tgt_platform: multiple
title: wmiadap
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35a58de2ca5e678cbbb99f803415572be236f2a545ed149b9ad598fb7f9a4664
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119049838"
---
# <a name="wmiadap"></a>wmiadap

Wmiadap ist eine Anwendung, die auf einem Windows, die Leistungsinformationen im WMI-Repository aktualisieren kann. Im Allgemeinen ermöglicht dies Entwicklern und IT-Administratoren das Erstellen von Skripts, die auf Leistungsinformationen zugreifen, z. B. die Menge an Arbeitsspeicher, die von einer Anwendung verwendet wird. Im folgenden Thema wird die Befehlszeilenschnittstelle beschrieben, mit der Sie steuern können, wie wmiadap Informationen abruft.

Wmiadap wird mit dem Betriebssystem auf den meisten Systemen im Verzeichnis C: Windows \\ \\ System32 \\ wbem installiert. Wenn Fehlermeldungen in Bezug auf wmiadap.exe angezeigt werden, suchen Sie [Microsoft-Support](https://support.microsoft.com/). Im Allgemeinen sollten Sie keine wmiadap.exe aus Ihrem System löschen, sofern nicht anders angegeben.

Die Übertragung von Daten aus den Leistungsbibliotheken und die Aktualisierung von Klassen, die von [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) und [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) abgeleitet wurden, erfolgt durch die [Anbieter WmiPerfClass](wmi-providers.md) und [WMIPerfInst.](wmi-providers.md) Der WmiPerfClass-Anbieter aktualisiert [WMI-Leistungsindikatorklassen nur,](/windows/desktop/CIMWin32Prov/performance-counter-classes) wenn ein neues Leistungsobjekt hinzugefügt wird. Sie können Wmiadap weiterhin mit dem **Schalter /r** ausführen, um die Treibertreiber Windows treibermodellieren, um Leistungsobjekte zu erstellen. Der **Schalter /f** erzwingt weiterhin eine Aktualisierung der WMI-Klassen aus den Leistungsbibliotheken.

Die folgenden Schalter sind an der Eingabeaufforderung verfügbar.

**wmiadap** \[ **/f** \] \[ **/r**\]

## <a name="switches"></a>Switches

<dl> <dt>

<span id="_f"></span><span id="_F"></span>**F**
</dt> <dd>

Analysiert alle Leistungsbibliotheken im System und aktualisiert die von [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) und [**Win32 \_ PerfFormattedData abgeleiteten Klassen.**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata)

</dd> <dt>

<span id="_r"></span><span id="_R"></span>**/r**
</dt> <dd>

Analysiert alle Treibertreiber Windows Treibermodells auf dem System, um Leistungsobjekte zu erstellen.

</dd> </dl>

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Leistungsbibliotheken und WMI](performance-libraries-and-wmi.md)
</dt> <dt>

[**winmgmt**](winmgmt.md)
</dt> </dl>

 

 
