---
title: Vermeiden des Ausblendens von Informationen
description: Gelegentlich blenden Programme absichtlich oder versehentlich Informationen aus der RPC-Marshalling-Engine aus.
ms.assetid: 016b9221-092d-4c25-a396-4f41dcdfb3cf
keywords:
- 64-Bit-Windows-Programmierung mit Abwärtskompatibilität
- Kompatibilitätsprobleme bei der 64-Bit-Windows-Programmierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e68ab20ccf267fed187488e4ec2a4d740492338fa1758703827101bd9b98bd3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119132863"
---
# <a name="avoiding-information-hiding"></a>Vermeiden des Ausblendens von Informationen

Gelegentlich blenden Programme absichtlich oder versehentlich Informationen aus der RPC-Marshalling-Engine aus. Einige Beispiele:

-   Senden einer Datenstruktur als undifferenzierter Byteblock
-   Nutzen der Leistung mithilfe eines Nebeneffekts einer Methode zum Kanalisieren zusätzlicher Daten über das Kabel
-   Versuch, ein Handle zu verdecken, indem es als **DWORD** oder **ULONG** übergeben wird

Diese Techniken führen fast garantiert zu Kompatibilitätsproblemen, noch bevor Sie Ihre Anwendung auf 64-Bit-Windows portieren.

Anstatt einen Serverkontext als **DWORD** in einem Standard-Remoteprozeduraufruf zu senden, verwenden Sie ein Kontexthandle, um ein nicht transparentes Handle für einen Serverkontext bereitzustellen, der im Auftrag eines Clients gespeichert wird. Kontexte werden durch GUIDs identifiziert, die durch die RPC-Laufzeit definiert werden, wenn ein Server ein Kontexthandle für einen Client erstellt. Es wird kein Zeiger über das Kabel verwendet, und der Vorgang ist über 32- oder 64-Bit-Grenzen hinweg vollständig transparent. Weitere Informationen zur Verwendung von Kontexthandles finden Sie unter [Kontexthandles.](/windows/desktop/Rpc/context-handles)

DCOM-Schnittstellen können keine Kontexthandles verwenden, da COM eine eigene Kontextverwaltung bereitstellt. Anstatt ein Kontexthandle zu erstellen, können Sie einen Schnittstellenzeiger an das COM-Objekt übergeben. Anschließend können Sie die Methoden direkt über den Schnittstellenzeiger aufrufen oder den Zeiger in andere Aufrufe platzieren. Um das Serverobjekt freizugeben, ruft der Client die **Release-Methode** der Schnittstelle über den Schnittstellenzeiger auf.

Auch hier kann es vorkommen, dass Sie den ursprünglichen Codeentwurf, den Sie portieren, nicht ändern können. Wenn es keine Möglichkeit gibt, das Senden eines Zeigers über das Kabel als **DWORD** zu vermeiden, müssen Sie eine Form der serverseitigen Zuordnung zwischen **DWORD-Werten** und Zeigern implementieren. Eine Möglichkeit hierzu besteht darin, die Zeiger in der clientseitigen Anwendung in Zeigergenauigkeitstypen wie **ULONG \_ PTR** oder **DWORD \_ PTR** zu ändern. Verwenden Sie dann den MIDL-Aufruf \[ [**\_ als**](/windows/desktop/Midl/call-as) \] Attribut, um die Zeiger als **DWORD-Werte** in die Leitung zu setzen. Der clientseitige Wrapper muss nur die Argumente übergeben. Der serverseitige Wrapper übernimmt die Zuordnung zwischen beiden Typen. Auf ähnliche Weise können Sie entweder die \[ [**Übertragung \_ als**](/windows/desktop/Midl/transmit-as) \] Attribut oder die Darstellung \[ [**\_ als**](/windows/desktop/Midl/represent-as) Attribut verwenden, um Ihre Daten in \] ein abwärtskompatibles Format für die Wire-Darstellung zu konvertieren.

Wenn die Abwärtskompatibilität kein Problem ist oder das Handle nicht für Remoteaufrufe verwendet wird und Sie sicher sind, dass Remoteaufrufe zwischen 32- und 64-Bit-Prozessen nie erfolgen, können Sie ein Argument als **ULONG64** neu definieren. Bei Bedarf können Sie die 32-Bit-Anwendung ändern, um ein **DWORD** an den Benutzer zu übergeben. Alternativ können Sie separate Stubs aus separaten IDL-Dateien für jede Plattform erstellen, indem Sie ein **DWORD** auf 32-Bit-Windows und ein **ULONG64** auf 64-Bit-Windows verwenden.

 

 