---
description: Eine der ersten Aufgaben, die Sie für einen Anbieter codieren müssen, ist der Initialisierungsprozess, der alle Aufgaben abdeckt, die Ihr Anbieter ausführen muss, die es ihm ermöglichen, Informationen von WMI zu senden und zu empfangen, ein verwaltetes Objekt zu steuern und andere Aufgaben auszuführen.
ms.assetid: 3dc145b8-1ce4-4caa-b2ac-31a3681e76f1
ms.tgt_platform: multiple
title: Initialisieren eines Anbieters
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e373cf72d4715919a9d7fc59064d156e80a1f2371c585d698a7c6edff4f22fa5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120097280"
---
# <a name="initializing-a-provider"></a>Initialisieren eines Anbieters

Eine der ersten Aufgaben, die Sie für einen Anbieter codieren müssen, ist der Initialisierungsprozess, der alle Aufgaben abdeckt, die Ihr Anbieter ausführen muss, die es ihm ermöglichen, Informationen von WMI zu senden und zu empfangen, ein verwaltetes Objekt zu steuern und andere Aufgaben auszuführen. Jeder Anbietertyp verfügt über einen anderen Satz von Aufgaben, die ausgeführt werden müssen, und verfügt über einen zugehörigen Satz eindeutiger Schnittstellen.

Alle Anbieter initialisieren jedoch über die [**IWbemProviderInit-Schnittstelle**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) und informieren WMI über ihren Initialisierungsstatus über die [**IWbemProviderInitSink-Schnittstelle.**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinitsink)

Im folgenden Verfahren wird beschrieben, wie ein Anbieter initialisiert wird.

**So initialisieren Sie einen Anbieter**

1.  Implementieren Sie [**IWbemProviderInit::Initialize**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinit-initialize) für Ihren Anbieter.

    Wenn WMI feststellt, dass ein Client die Dienste eines Anbieters benötigt, lädt WMI den Anbieter, indem die [**IWbemProviderInit::Initialize-Methode**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinit-initialize) aufgerufen wird.

2.  Implementieren Sie alle Schnittstellen, die für Ihren Anbietertyp eindeutig sind.
3.  Informieren Sie WMI, dass die Initialisierung Ihres Anbieters abgeschlossen ist, indem [**Sie IWbemProviderInitSink::SetStatus**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinitsink-setstatus)aufrufen.

    Alle Implementierungen von [**IWbemProviderInit::Initialize**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinit-initialize) müssen [**IWbemProviderInitSink::SetStatus**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinitsink-setstatus) aufrufen, um den Initialisierungsstatus an WMI zu melden. Mit der **SetStatus-Methode** kann WMI bestimmen, ob ein Anbieter zum Empfangen von Anforderungen bereit ist und welche Art von Anforderungen der Anbieter empfangen kann.

Im folgenden Verfahren wird beschrieben, wie sie eine erfolgreiche Initialisierung melden.

**So melden Sie eine erfolgreiche Initialisierung**

-   Legen Sie den *IStatus-Parameter* von [**SetStatus**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinitsink-setstatus) auf **WBEM \_ S \_ INITIALIZED fest.**

    Durch die Rückgabe von **WBEM \_ S \_ INITIALIZED** gibt ein Anbieter die Bereitschaft an, Anforderungen von Anwendungen, WMI und anderen Anbietern zu verarbeiten. Nachdem WBEM \_ S \_ INITIALIZED empfangen wurde, ruft WMI die [**IWbemProviderInit::QueryInterface-Methode**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) für den Anbieter auf. Diese Abfrage ruft einen Zeiger auf die primäre Schnittstelle des Anbieters ab.

Im folgenden Verfahren wird beschrieben, wie sie während der Initialisierung einen Fehler melden.

**So melden Sie einen Fehler während der Initialisierung**

-   Legen Sie den *IStatus-Parameter* von [**SetStatus**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinitsink-setstatus) auf **WBEM \_ E \_ FAILED** fest. WMI betrachtet Anbieter, die **WBEM \_ E \_ FAILED** zurückgeben, als nicht funktionsfähig.

    WMI gibt den [**IWbemProviderInit-Zeiger**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) entweder frei, nachdem WMI einen Zeiger auf die primäre Schnittstelle des Anbieters abgerufen hat oder nachdem die Initialisierung fehlgeschlagen ist.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Entwickeln eines WMI-Anbieters](developing-a-wmi-provider.md)
</dt> <dt>

[Festlegen von Namepace-Sicherheitsbeschreibungen](setting-namespace-security-descriptors.md)
</dt> <dt>

[Schützen Ihres Anbieters](securing-your-provider.md)
</dt> </dl>

 

 



