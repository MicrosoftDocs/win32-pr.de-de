---
description: WIA wird als out-of-process-Server (COM) Component Object Model implementiert, um den stabilen Betrieb von Clientanwendungen sicherzustellen.
ms.assetid: 9f3d1848-36ab-4e0f-a7f4-312bc85ecc00
title: WIA-Architektur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 159a6bb88fba5a79f2915500786bbfcf8d531bfe0170ec6c6841f419425ee296
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119813264"
---
# <a name="wia-architecture"></a>WIA-Architektur

WIA wird als out-of-process-Server (COM) Component Object Model implementiert, um den stabilen Betrieb von Clientanwendungen sicherzustellen. Im Gegensatz zu den meisten Out-of-Process-Serveranwendungen vermeidet Windows Image Acquisition (WIA) Leistungsnachgaben während der Bilddatenübertragung, indem ein eigener Datenübertragungsmechanismus( [**IWiaDataTransfer**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatatransfer)) zur Verfügung stellt. Diese Hochleistungsschnittstelle verwendet ein Freigegebenes Speicherfenster, um Daten an den Client zu übertragen.

WIA verfügt über drei Hauptkomponenten: einen Geräte-Manager, eine Minidriver-Dienstbibliothek und einen Geräte-Minitreiber.

-   Der Geräte-Manager listet Bildverarbeitungsgeräte auf, ruft Geräteeigenschaften ab, richtet Ereignisse für Geräte ein und erstellt Geräteobjekte.
-   Die Minidriver-Dienstbibliothek implementiert alle geräteunabhängigen Dienste.
-   Der Geräte-Minitreiber ordnet WIA-Eigenschaften und -Befehle dem jeweiligen Gerät zu.

Das folgende Diagramm veranschaulicht die WIA-Architektur:

![wia-Architektur](images/wiarch.gif)

 

 



