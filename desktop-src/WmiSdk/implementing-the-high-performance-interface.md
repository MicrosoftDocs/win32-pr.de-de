---
description: Da WMI einen hochleistungsfähigen Anbieter in eine WMI-oder Client Anwendung lädt, müssen Sie den Hochleistungs Anbieter als Prozess interner Server entwerfen.
ms.assetid: c37e3652-8c76-4125-ba62-ae860858797e
ms.tgt_platform: multiple
title: Implementieren der High-Performance-Schnittstelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ea6e7f75e1031caacbb7379fba025baceb7b1a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106347703"
---
# <a name="implementing-the-high-performance-interface"></a>Implementieren der High-Performance-Schnittstelle

Da WMI einen hochleistungsfähigen Anbieter in eine WMI-oder Client Anwendung lädt, müssen Sie den Hochleistungs Anbieter als Prozess interner Server entwerfen. Außerdem müssen Sie die Hochleistungs Anbieter Methoden in den Schnittstellen [**IWbemHiPerfProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemhiperfprovider) und [**iwbemaktusher**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemrefresher) implementieren.

Implementieren Sie einen Hochleistungs Anbieter als in-Process-Server. Eine Funktion, die Sie bei der Implementierung der Sicherheit eines in-Process-Servers berücksichtigen sollten, ist die Art und Weise, in der der Anbieter seinen eigenen Speicherort identifiziert. Beim Laden von "in-Process" in WMI instanziiert WMI den Anbieter mithilfe einer CLSID. Wenn die Client Anwendung im Prozess in eine Client Anwendung geladen wird, instanziiert Sie den Anbieter mit der **clientloadableclsid** -Eigenschaft. Wenn Sie einer CLSID und **clientloadableclsid** unterschiedliche Werte geben, können Sie den Anbieter ermitteln, ob er in-Process in WMI oder in eine Client Anwendung geladen wird. Wenn Sie sich in einem WMI-Prozess befinden, sollte der Anbieter alle notwendigen Client Identitätswechsel mithilfe von **clientloadableclsid** durchführen. Wenn Sie sich in einem Client Prozess befinden, erbt der Anbieter das Zugriffs Token des Threads, für den er aufgerufen wird. Weitere Informationen zum Implementieren eines in-Process-Servers finden Sie im [Abschnitt zu com](https://msdn.microsoft.com/library/aa139695.aspx) in MSDN.

Als Prozess interner Server verwendet ein Hochleistungs Anbieter ein Aktualisierungs Objekt, um Daten für den Remote Client aktuell zu halten. In der folgenden Tabelle sind die Methoden aufgeführt, die Sie für einen Hochleistungs Anbieter implementieren müssen.



| Methode                                                                                              | Funktion                                           |
|-----------------------------------------------------------------------------------------------------|---------------------------------------------------|
| [**IWbemHiPerfProvider:: queryinstance**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-queryinstances)                   | Abfragen                                           |
| [**IWbemHiPerfProvider:: GetObjects**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-getobjects)                           | Objekt Abruf                                  |
| [**IWbemHiPerfProvider:: "kreaterefresher"**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-createrefresher)                 | Erstellt ein Aktualisierungs Programm                               |
| [**IWbemHiPerfProvider:: kreaterefreshableobject**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-createrefreshableobject) | Erstellt ein Aktualisier bares Instanzobjekt.             |
| [**IWbemHiPerfProvider:: Aufzählung**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-createrefreshableenum)     | Erstellt einen aktualisierbaren Enumerator.                  |
| [**IWbemHiPerfProvider:: stopaktualisieren**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-stoprefreshing)                   | Beendet das Aktualisieren eines Enumerators oder Instanzobjekts. |
| [**Iwbemrefresh Sher:: Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh)                                           | Erstellt ein Aktualisierungs Programm                               |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erstellen eines Instanzanbieters in einen High-Performance-Anbieter](making-an-instance-provider-into-a-high-performance-provider.md)
</dt> </dl>

 

 



