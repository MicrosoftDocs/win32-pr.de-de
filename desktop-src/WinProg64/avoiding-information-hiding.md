---
title: Vermeiden von Informationen ausblenden
description: Gelegentlich Blenden Programme absichtlich oder versehentlich Informationen aus der RPC-Marshalling-Engine aus.
ms.assetid: 016b9221-092d-4c25-a396-4f41dcdfb3cf
keywords:
- Abwärtskompatibilität 64-Bit-Windows-Programmierung
- Kompatibilitätsprobleme 64-Bit-Windows-Programmierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f4b9e4ba7ed5165378beb93005243af03f9e469
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390579"
---
# <a name="avoiding-information-hiding"></a>Vermeiden von Informationen ausblenden

Gelegentlich Blenden Programme absichtlich oder versehentlich Informationen aus der RPC-Marshalling-Engine aus. Einige Beispiele:

-   Senden einer Datenstruktur als undifferenzierter Block von Bytes
-   Nutzen der Leistung durch einen Nebeneffekt aus einer Methode, um zusätzliche Daten über das Netzwerk zu leiten
-   Es wird versucht, ein Handle zu verbergen, indem es als **DWORD** oder **ulong** übergeben wird.

Diese Techniken stellen fast garantiert Kompatibilitätsprobleme dar, bevor Sie Ihre Anwendung auf 64-Bit-Windows portieren.

Anstatt einen Server Kontext als **DWORD** in einem standardmäßigen Remote Prozedur aufrufsend zu senden, verwenden Sie ein Kontext Handle, um ein nicht transparentes Handle für einen Server Kontext bereitzustellen, der im Auftrag eines Clients gespeichert wird. Kontexte werden durch GUIDs identifiziert, die von der RPC-Laufzeit definiert werden, wenn ein Server ein Kontext Handle für einen Client erstellt. Kein Zeiger wird über das Netzwerk verwendet, und der Vorgang ist vollständig über 32-oder 64-Bit-Grenzen hinweg transparent. Weitere Informationen zur Verwendung von Kontext Handles finden Sie unter [Kontext Handles](/windows/desktop/Rpc/context-handles).

DCOM-Schnittstellen können keine Kontext Handles verwenden, da com eine eigene Kontext Verwaltung bereitstellt. Anstatt ein Kontext Handle zu erstellen, können Sie einen Schnittstellen Zeiger an das COM-Objekt übergeben. Anschließend können Sie die Methoden direkt über den Schnittstellen Zeiger aufrufen oder den Zeiger in anderen aufrufen platzieren. Um das Server Objekt freizugeben, ruft der Client die **releasemethode** der Schnittstelle über den Schnittstellen Zeiger auf.

Auch hier kann es vorkommen, dass Sie den ursprünglichen Entwurf des Codes, den Sie portieren, nicht ändern können. Wenn es keine Möglichkeit gibt, einen Zeiger über das Netzwerk als **DWORD** zu senden, müssen Sie eine Form der serverseitigen Zuordnung zwischen **DWORD** -Werten und Zeigern implementieren. Eine Möglichkeit besteht darin, die Zeiger in der Client seitigen Anwendung in Typen von Zeiger Genauigkeit zu ändern, wie z. b. **ulong \_ ptr** oder **DWORD \_ ptr**. Verwenden Sie dann den Mittel \[ Wert " [**\_ Callas**](/windows/desktop/Midl/call-as) "- \] Attribut, um die Zeiger als **DWORD** -Werte in das Netzwerk zu versetzen. Vom Client seitigen Wrapper müssen die Argumente nur an übergeben werden. Der serverseitige Wrapper verarbeitet die Zuordnung zwischen beiden Typen. Auf ähnliche Weise können Sie entweder das Attribut "über \[ [**tragen \_ als**](/windows/desktop/Midl/transmit-as) " \] oder das \[ Attribut " [**\_ As**](/windows/desktop/Midl/represent-as) " verwenden \] , um Ihre Daten in ein abwärts kompatibles Format für die Wire-Darstellung zu konvertieren.

Wenn die abwärts Netzwerkkompatibilität kein Problem ist oder das Handle nicht für Remote Aufrufe verwendet wird und Sie sicher sind, dass Remote Aufrufe zwischen 32-und 64-Bit-Prozessen nie ausgeführt werden, können Sie ein Argument als **ULONG64** neu definieren. Falls erforderlich, können Sie die 32-Bit-Anwendung so ändern, dass ein **DWORD** an den Benutzer übergeben wird. Alternativ können Sie separate stubvorgänge aus separaten IDL-Dateien für jede Plattform erstellen, indem Sie ein **DWORD** auf 32-Bit-Fenstern und eine **ULONG64** auf 64-Bit-Windows verwenden.

 

 