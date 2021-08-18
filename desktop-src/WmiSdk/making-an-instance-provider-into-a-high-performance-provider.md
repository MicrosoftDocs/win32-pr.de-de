---
description: Das Schreiben eines WMI-Hochleistungsanbieters zum Erstellen von Leistungsindikatoren wird nicht empfohlen.
ms.assetid: 6a22d6f7-d9e2-45fa-876d-921a4bc4f574
ms.tgt_platform: multiple
title: Erstellen eines Instanzanbieters zu einem High-Performance Anbieter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2b6326c0af270088c37bb2a1798951ba0a9de7afe65ec593f5f7ab6768b83b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119996490"
---
# <a name="making-an-instance-provider-into-a-high-performance-provider"></a>Erstellen eines Instanzanbieters zu einem High-Performance Anbieter

Das Schreiben eines WMI-Hochleistungsanbieters zum Erstellen von Leistungsindikatoren wird nicht empfohlen. Ab Windows Vista werden die [](/windows/desktop/CIMWin32Prov/performance-counter-classes) WMI-Leistungsindikatorklassen nicht mehr vom Reverseadapter AutoDiscovery/AutoPurge (ADAP) in die Windows-Leistungsbibliotheken migriert. Verwenden Sie zum Erstellen eines Leistungsindikatoranbieters [Die Leistungsindikatoren Version 2.0.](/windows/desktop/PerfCtrs/performance-counters-portal) Nachdem Leistungsbibliotheksobjekte erstellt wurden, analysiert [der WMIPerfClass-Anbieter](wmiperfclass-provider.md) die Objekte und erstellt oder aktualisiert eine von [**Win32 \_ Perf**](/windows/desktop/CIMWin32Prov/win32-perf) abgeleitete WMI-Klasse für jedes Leistungsobjekt. Der [WMIPerfInst-Anbieter](wmiperfinst-provider.md) stellt dann dynamisch unformatierte und formatierte Leistungsindikatordaten für die WMI-Leistungsklassen zur Verfügung.

Das folgende verfahren auf hoher Ebene enthält die erforderlichen Schritte zum Erstellen eines Hochleistungsanbieters.

**So erstellen Sie einen Hochleistungsanbieter**

1.  Registrieren Sie Ihren Anbieter bei WMI. Weitere Informationen finden Sie unter [Registrieren eines High-Performance Anbieters.](registering-a-high-performance-provider.md)
2.  Implementieren Sie Ihren Anbieter. Weitere Informationen finden Sie unter [Schreiben eines Instanzanbieters.](writing-an-instance-provider.md)
3.  Implementieren Sie die Hochleistungsschnittstelle. Weitere Informationen finden Sie unter [Implementieren der High-Performance-Schnittstelle.](implementing-the-high-performance-interface.md)
4.  Leiten Sie Ihr MOF-Schema (Managed Object Format) ab, und schreiben Sie es, um rohe Leistungsdaten zu erhalten. Weitere Informationen finden Sie unter [Supporting the Win32 \_ PerfRawData Class](supporting-the-win32-perfrawdata-class.md).
5.  Leiten Sie Ihr MOF-Schema ab, und schreiben Sie es, um vorab berechnete Daten zu erhalten. Durch die Unterstützung dieser Klasse ist der Anbieter nicht erforderlich, um die Berechnungen durchzuführen. Diese Daten sind dieselben, die im Systemmonitor in Perfmon angezeigt werden. Weitere Informationen finden Sie unter [Supporting the Win32 \_ PerfFormattedData Class](supporting-the-win32-perfformatteddata-class.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Entwickeln eines WMI-Anbieters](developing-a-wmi-provider.md)
</dt> <dt>

[Leistungsbibliotheken und WMI](performance-libraries-and-wmi.md)
</dt> </dl>

 

 
