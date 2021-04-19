---
description: Das Schreiben eines hochleistungsfähigen WMI-Anbieters zum Erstellen von Leistungsindikatoren ist nicht empfehlenswert.
ms.assetid: 6a22d6f7-d9e2-45fa-876d-921a4bc4f574
ms.tgt_platform: multiple
title: Erstellen eines Instanzanbieters in einen High-Performance-Anbieter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10744b110463a3207f76bb55d48a8045ec22783d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363496"
---
# <a name="making-an-instance-provider-into-a-high-performance-provider"></a>Erstellen eines Instanzanbieters in einen High-Performance-Anbieter

Das Schreiben eines hochleistungsfähigen WMI-Anbieters zum Erstellen von Leistungsindikatoren ist nicht empfehlenswert. Ab Windows Vista werden die WMI- [Leistungs Leistungs](/windows/desktop/CIMWin32Prov/performance-counter-classes) Daten-Klassen nicht mehr vom reverseadapter AutoDiscovery/AUTOPURGE (ADAP) in die Windows-Leistungs Bibliotheken migriert. Verwenden Sie zum Erstellen eines Leistungsindikator Anbieters die [Leistungsindikatoren Version 2,0](/windows/desktop/PerfCtrs/performance-counters-portal). Nachdem Leistungs Bibliotheksobjekte erstellt wurden, analysiert der [wmiperfclass-Anbieter](wmiperfclass-provider.md) die Objekte und erstellt oder aktualisiert eine von [**Win32 \_ perf**](/windows/desktop/CIMWin32Prov/win32-perf) abgeleitete WMI-Klasse für jedes Leistungs Objekt. Der [WMIPerfInst-Anbieter](wmiperfinst-provider.md) stellt dann dynamisch Rohdaten und formatierte Leistungsdaten für die WMI-Leistungsklassen bereit.

Die folgende allgemeine Vorgehensweise enthält die zum Erstellen eines Hochleistungs Anbieters erforderlichen Schritte.

**So erstellen Sie einen Hochleistungs Anbieter**

1.  Registrieren Sie Ihren Anbieter bei WMI. Weitere Informationen finden Sie unter [Registrieren eines High-Performance Anbieters](registering-a-high-performance-provider.md).
2.  Implementieren Sie Ihren Anbieter. Weitere Informationen finden Sie unter [Schreiben eines Instanzanbieters](writing-an-instance-provider.md).
3.  Implementieren Sie die Hochleistungs Schnittstelle. Weitere Informationen finden Sie unter [Implementieren der High-Performance-Schnittstelle](implementing-the-high-performance-interface.md).
4.  Leiten Sie das MOF-Schema (Managed Object Format) ab, und schreiben Sie es, um rohleistungs Daten abzurufen. Weitere Informationen finden Sie [unter unterstützen der Win32 \_ perfrawdata-Klasse](supporting-the-win32-perfrawdata-class.md).
5.  Ableiten und schreiben Sie das MOF-Schema, um vorab berechnete Daten zu erhalten. Wenn diese Klasse unterstützt wird, ist es nicht erforderlich, dass der Anbieter die Berechnungen ausführt. Dabei handelt es sich um die gleichen Daten, die im System Monitor in Perfmon angezeigt werden. Weitere Informationen finden Sie [unter unterstützen der Win32 \_ perfformatteddata-Klasse](supporting-the-win32-perfformatteddata-class.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Entwickeln eines WMI-Anbieters](developing-a-wmi-provider.md)
</dt> <dt>

[Leistungs Bibliotheken und WMI](performance-libraries-and-wmi.md)
</dt> </dl>

 

 
