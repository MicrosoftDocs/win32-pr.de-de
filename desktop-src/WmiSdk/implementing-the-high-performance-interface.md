---
description: Da WMI einen leistungsstarken Anbieter in einem Prozess in WMI oder in eine Clientanwendung lädt, müssen Sie Ihren Hochleistungsanbieter als In-Process-Server entwerfen.
ms.assetid: c37e3652-8c76-4125-ba62-ae860858797e
ms.tgt_platform: multiple
title: Implementieren der High-Performance-Schnittstelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecec9a7b5e5399765adaa7a0e195825493d930ece46c30af3e788795fe08ebf8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118108621"
---
# <a name="implementing-the-high-performance-interface"></a>Implementieren der High-Performance-Schnittstelle

Da WMI einen leistungsstarken Anbieter in einem Prozess in WMI oder in eine Clientanwendung lädt, müssen Sie Ihren Hochleistungsanbieter als In-Process-Server entwerfen. Darüber hinaus müssen Sie die Hochleistungsanbietermethoden in den Schnittstellen [**IWbemHiPerfProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemhiperfprovider) und [**IWbemRefresher**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemrefresher) implementieren.

Sie sollten einen Hochleistungsanbieter als In-Process-Server implementieren. Ein Feature, das Sie beim Implementieren der Sicherheit eines In-Process-Servers beachten sollten, ist die Art und Weise, wie der Anbieter seinen eigenen Standort identifiziert. Beim Laden im Prozess in WMI instanziiert WMI den Anbieter mithilfe einer CLSID. Beim Laden in eine Clientanwendung instanziiert die Clientanwendung den Anbieter mit der **ClientLoadableCLSID-Eigenschaft.** Indem Sie einer CLSID und **ClientLoadableCLSID** unterschiedliche Werte geben, können Sie dem Anbieter ermöglichen, zu bestimmen, ob er prozessübergreifend in WMI oder in eine Clientanwendung geladen wird. Wenn sich der Anbieter in einem WMI-Prozess befindet, sollte er den erforderlichen Clientidentitätswechsel mithilfe von **ClientLoadableCLSID** durchführen. Wenn sich der Anbieter in einem Clientprozess befindet, erbt er das Zugriffstoken des Threads, für den er aufgerufen wird. Weitere Informationen zum Implementieren eines In-Process-Servers finden Sie im [COM-Abschnitt](https://msdn.microsoft.com/library/aa139695.aspx) von MSDN.

Als In-Process-Server verwendet ein Hochleistungsanbieter ein Aktualisierungsobjekt, um die Daten für den Remoteclient auf dem aktuellen Stand zu halten. In der folgenden Tabelle sind die Methoden aufgeführt, die Sie für einen Hochleistungsanbieter implementieren müssen.



| Methode                                                                                              | Komponente                                           |
|-----------------------------------------------------------------------------------------------------|---------------------------------------------------|
| [**IWbemHiPerfProvider::QueryInstances**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-queryinstances)                   | Abfragen                                           |
| [**IWbemHiPerfProvider::GetObjects**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-getobjects)                           | Objektabruf                                  |
| [**IWbemHiPerfProvider::CreateRefresher**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-createrefresher)                 | Erstellt eine Aktualisierung                               |
| [**IWbemHiPerfProvider::CreateRefreshableObject**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-createrefreshableobject) | Erstellt ein aktualisierbares Instanzobjekt.             |
| [**IWbemHiPerfProvider::CreateRefreshableEnum**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-createrefreshableenum)     | Erstellt einen aktualisierbaren Enumerator                  |
| [**IWbemHiPerfProvider::StopRefreshing**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-stoprefreshing)                   | Beendet das Aktualisieren eines Enumerators oder Instanzobjekts. |
| [**IWbemRefresher::Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh)                                           | Erstellt eine Aktualisierung                               |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erstellen eines Instanzanbieters zu einem High-Performance Anbieter](making-an-instance-provider-into-a-high-performance-provider.md)
</dt> </dl>

 

 



