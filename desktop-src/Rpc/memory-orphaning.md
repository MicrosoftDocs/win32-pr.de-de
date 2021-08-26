---
title: Verwaister Arbeitsspeicher
description: Wenn Ihre verteilte Anwendung einen \in-, out-, unique\- oder \in-, out-, ptr\-Zeigerparameter verwendet, kann die Serverseite der Anwendung den Wert des Zeigerparameters in NULL ändern.
ms.assetid: 65588b4d-6bf4-44f7-994c-29a5b185c6b9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a64b3a560eb1daecf3cd10bc18c62057cd2d09c1321c272f4e8fe73a65305832
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120019828"
---
# <a name="memory-orphaning"></a>Verwaister Arbeitsspeicher

Wenn Ihre verteilte Anwendung einen \[ [in](/windows/desktop/Midl/in), [out](/windows/desktop/Midl/out-idl), [unique](/windows/desktop/Midl/unique) oder \] in \[ , **out**, [ptr-Zeigerparameter](/windows/desktop/Midl/ptr) verwendet, kann die Serverseite der Anwendung den Wert des Zeigerparameters in \] NULL ändern. Wenn der Server anschließend den NULL-Wert an den Client zurückgibt, ist der Arbeitsspeicher, auf den vom Zeiger vor dem Remoteprozeduraufruf verwiesen wird, weiterhin auf clientseitiger Seite vorhanden, kann jedoch nicht mehr von diesem Zeiger aus zugänglich sein (außer im Fall eines vollständigen Zeigers mit Alias). Dieser Arbeitsspeicher wird als *verwaist bezeichnet.* Dies wird auch als *Speicherverlust bezeichnet.* Wiederholtes Verwaisten des Arbeitsspeichers auf dem Client führt dazu, dass dem Client nicht genügend Arbeitsspeicherressourcen zur Verfügung stehen.

Der Arbeitsspeicher kann auch verwaist sein, wenn der Server einen eingebetteten Zeiger in einen NULL-Wert ändert. Wenn der Parameter beispielsweise auf eine komplexe Datenstruktur wie eine Struktur verweist, kann die Serverseite der Anwendung Knoten der Struktur löschen und Zeiger innerhalb der Struktur auf NULL festlegen.

Eine weitere Situation, die zu einem Speicherverlust führen kann, sind konforme, unterschiedliche und offene Arrays, die Zeiger enthalten. Wenn die Serveranwendung den Parameter ändert, der die Arraygröße oder den übertragenen Bereich angibt, sodass er einen kleineren Wert darstellt, verwenden die Stubs die kleineren Werte, um Arbeitsspeicher frei zu geben. Die Arrayelemente mit Indizes, die größer als der size-Parameter sind, sind verwaist. Ihre Anwendung muss Elemente außerhalb des übertragenen Bereichs frei geben.

 

 