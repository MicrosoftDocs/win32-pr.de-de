---
title: WFP-Architektur
description: Dieser Abschnitt bietet eine kurze Übersicht über die Architektur Windows Filterplattform.
ms.assetid: 17a90f5c-ef82-4b14-b7f1-dd025d5f7303
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41989a11ff5412b3185f6987f9588f0309c3fde3ca386c71e4613ab6bc8237f8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119766604"
---
# <a name="wfp-architecture"></a>WFP-Architektur

Die folgende Abbildung zeigt die grundlegende Architektur der Windows Filtering Platform (WFP).

![Grundlegende Architektur des Diagramms der Windows-Filterplattform](images/wfp-architecture.png)

## <a name="filter-engine"></a>Filter-Engine

Die Filter-Engine enthält eine Benutzermoduskomponente und eine Kernelmoduskomponente, die zusammen alle Filtervorgänge für Netzwerkdaten ausführen. Die Filter-Engine enthält mehrere Filterebenen, die den Netzwerkstapelebenen des Betriebssystems lose zuordnen. Die Filter-Engine-Ebenen werden basierend auf der Filter-Engine-Komponente, die sie besitzt, in Benutzermodusebenen und Kernelmodusebenen unterteilt.

Die Benutzermoduskomponente führt RPC- und IPsec-Filterung durch. Die Filter-Engine enthält ca. 10 Filterebenen im Benutzermodus.

Die Kernelmoduskomponente filtert die Netzwerk- und Transportebenen des TC/IP-Stapels. Diese Komponente ruft auch die verfügbaren Calloutfunktionen während des [Klassifizierungsprozesses](basic-operation.md) auf. Die Filter-Engine enthält ungefähr 50 Filterebenen im Kernelmodus.

Eine [**Beschreibung der einzelnen Filter-Engine-Ebenen**](management-filtering-layer-identifiers-.md) finden Sie unter Filtern von Ebenenbezeichnern.

## <a name="base-filtering-engine"></a>Basisfiltermodul

Die Basisfilterungs-Engine (Base Filtering Engine, BFE) ist ein Benutzermodusdienst (bfe.dll, der in einem svchost.exe-Prozess ausgeführt wird), der die WFP-Komponenten koordiniert. Die wichtigsten Aufgaben von BFE sind das Hinzufügen und Entfernen von Filtern aus dem System, das Speichern der Filterkonfiguration und das Erzwingen der WFP-Konfigurationssicherheit. Anwendungen kommunizieren mit BFE über die [WFP-Verwaltungsfunktionen.](fwp-mgmt-functions.md)

## <a name="callout-drivers"></a>Callout-Treiber

Callouttreiber bieten zusätzliche Filterfunktionen, indem sie der Filter-Engine auf einer oder mehreren Filterebenen im Kernelmodus benutzerdefinierte Calloutfunktionen hinzufügen. Callouts unterstützen eine tiefe Überprüfung und Paketüberprüfung sowie Streamänderungen. Nachdem ein Callouttreiber seine Calloutfunktionen zur Filter-Engine hinzugefügt hat, können Filter, die die Calloutfunktion eines bestimmten Treibers angeben, dem Filterprozess hinzugefügt werden. Solche Filter können entweder von einer Verwaltungsanwendung im Benutzermodus oder vom Callouttreiber selbst hinzugefügt werden. Die im Windows Development Kit bereitgestellte Kernelmodusschnittstelle sollte nur bei Bedarf und nicht als Ersatz für die Benutzermodus-API verwendet werden.

> [!Note]  
> Weitere Informationen zu Callouttreibern finden Sie im Abschnitt Windows Filtering Platform des [Windows Development Kit.](/windows-hardware/drivers/network/windows-filtering-platform-callout-drivers2)

 

Die Windows Filterplattform enthält eine Reihe von integrierten Rückruffunktionen, die für die sichere IPsec-Datenkommunikation, zustandsbehaftete Filtereinstellungen und filterung im geschützten Modus verwendet werden können. Eine [**vollständige Liste der integrierten Calloutfunktionen**](built-in-callout-identifiers.md) finden Sie unter Integrierte Aufrufbezeichner.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Objektmodell](object-model.md)
</dt> <dt>

[WFP-Vorgang](basic-operation.md)
</dt> <dt>

[Windows Filtern von Plattformaufruftreibern – Entwurfshandbuch](/windows-hardware/drivers/network/windows-filtering-platform-callout-drivers2)
</dt> <dt>

[Windows Filtern von Plattform-Callouttreibern – Referenz](/windows-hardware/drivers/ddi/_netvista/)
</dt> </dl>

 

 