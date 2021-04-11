---
title: WFP-Architektur
description: Dieser Abschnitt enthält eine kurze Übersicht über die Architektur der Windows-Filter Plattform.
ms.assetid: 17a90f5c-ef82-4b14-b7f1-dd025d5f7303
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8740fed254aca97ab77566e2a7f0ace9a6679d56
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104209178"
---
# <a name="wfp-architecture"></a>WFP-Architektur

Die folgende Abbildung zeigt die grundlegende Architektur der Windows-Filter Plattform (WFP).

![grundlegende Architektur des Windows-Filter Platt Form Diagramms](images/wfp-architecture.png)

## <a name="filter-engine"></a>Filter-Engine

Die Filter-Engine enthält eine Benutzermoduskomponente und eine Kernelmoduskomponente, die alle Filter Vorgänge für Netzwerkdaten ausführt. Die Filter-Engine enthält mehrere Filter Ebenen, die den Netzwerk Stapel Ebenen des Betriebssystems lose zugeordnet werden. Die Filter-Engine-Ebenen werden basierend auf der Filter-Engine-Komponente, die Sie besitzt, in benutzermodusebenen und Kernel Modus-Ebenen aufgeteilt.

Die Benutzermoduskomponente führt RPC-und IPSec-Filterung aus. Die Filter-Engine enthält ungefähr 10 Benutzermodus-Filter Ebenen.

Die Kernelmoduskomponente führt das Filtern auf der Netzwerk-und Transport Ebene des TC/IP-Stapels durch. Diese Komponente ruft während des [Klassifizierungs](basic-operation.md) Prozesses auch die verfügbaren Legenden Funktionen auf. Die Filter-Engine enthält ungefähr 50 Kernel Modus-Filter Ebenen.

Unter [**Filtern von ebenenbezeichern**](management-filtering-layer-identifiers-.md) finden Sie eine Beschreibung der einzelnen Filter-Engine-Ebenen.

## <a name="base-filtering-engine"></a>Basisfiltermodul

Die Basis Filter-Engine (Basis Filter-Engine, BFE) ist ein Dienst im Benutzermodus (bfe.dll in einem svchost.exe Prozess ausgeführt), der die WFP-Komponenten koordiniert. Die Prinzipal Aufgaben, die von BFE durchgeführt werden, sind das Hinzufügen und Entfernen von Filtern aus dem System, das Speichern der Filter Konfiguration und das Erzwingen der WFP Anwendungen kommunizieren über die [WFP-Verwaltungsfunktionen](fwp-mgmt-functions.md)mit BFE.

## <a name="callout-drivers"></a>Callout-Treiber

Legenden-Treiber bieten zusätzliche Filter Funktionalität durch Hinzufügen von benutzerdefinierten Legenden Funktionen zur Filter-Engine auf einer oder mehreren kernelmodusfilterungs-Ebenen. Callouts unterstützen tiefgreifende Überprüfungen und Pakete sowie Datenstrom Änderungen. Nachdem ein Legenden Treiber seine Legenden Funktionen zur Filter-Engine hinzugefügt hat, können Filter, die die Legenden-Funktion eines bestimmten Treibers angeben, dem Filter Vorgang hinzugefügt werden. Solche Filter können entweder von einer Verwaltungs Anwendung im Benutzermodus oder vom Legenden Treiber selbst hinzugefügt werden. Die im Windows Development Kit gelieferte kernelmodusschnittstelle sollte nur bei Bedarf verwendet und nicht als Ersatz für die benutzermodusapi verwendet werden.

> [!Note]  
> Weitere Informationen zu Legenden Treibern finden Sie im Abschnitt Windows-Filter Plattform des [Windows Development Kits](/windows-hardware/drivers/network/windows-filtering-platform-callout-drivers2).

 

Die Windows-Filter Plattform enthält eine Reihe integrierter Legenden Funktionen, die für die sichere IPSec-Datenkommunikation, Zustands behaftete Filtereinstellungen und das Filtern im verborgenen Modus verwendet werden können. Eine komplette Liste der integrierten Legenden Funktionen finden Sie unter [**integrierte**](built-in-callout-identifiers.md) Legenden Bezeichner.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Objektmodell](object-model.md)
</dt> <dt>

[WFP-Vorgang](basic-operation.md)
</dt> <dt>

[Windows-Filter Plattform-Callout-Treiber-Entwurfs Handbuch](/windows-hardware/drivers/network/windows-filtering-platform-callout-drivers2)
</dt> <dt>

[Windows-Filter Plattform-Callout-Treiber-Referenz](/windows-hardware/drivers/ddi/_netvista/)
</dt> </dl>

 

 