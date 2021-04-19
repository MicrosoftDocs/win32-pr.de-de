---
title: Arbeitsspeicher verwaisen
description: Wenn Ihre verteilte Anwendung den Parameter \ in, out, Unique \ oder \ in, out, PTR \ Pointer verwendet, kann die Serverseite der Anwendung den Wert des Zeiger Parameters in NULL ändern.
ms.assetid: 65588b4d-6bf4-44f7-994c-29a5b185c6b9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32042911695f377e0a628168e91387bfa25f0d79
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106341960"
---
# <a name="memory-orphaning"></a>Arbeitsspeicher verwaisen

Wenn Ihre verteilte Anwendung einen \[ [in](/windows/desktop/Midl/in)-, [out](/windows/desktop/Midl/out-idl)-, [Unique](/windows/desktop/Midl/unique) - \] oder \[ **in**-, **out**-, [ptr](/windows/desktop/Midl/ptr) - \] Zeiger Parameter verwendet, kann die Serverseite der Anwendung den Wert des Zeiger Parameters in NULL ändern. Wenn der Server anschließend den NULL-Wert an den Client zurückgibt, ist der Speicher, auf den der Zeiger vor dem Remote Prozedur Aufruf verweist, auf der Clientseite immer noch vorhanden, aber nicht mehr über diesen Zeiger zugänglich (außer bei einem vollständigen Zeiger mit Alias). Dieser Speicher wird als *verwaist* bezeichnet. Dies wird auch als *Speicherlecks* bezeichnet. Das wiederholte verwaisen des Speichers auf dem Client bewirkt, dass der Client nicht mehr über genügend Speicherressourcen verfügt.

Der Arbeitsspeicher kann auch dann verwaist werden, wenn der Server einen eingebetteten Zeiger auf einen NULL-Wert ändert. Wenn der-Parameter z. b. auf eine komplexe Datenstruktur, z. b. eine-Struktur, verweist, kann die Serverseite der Anwendung Knoten der Struktur löschen und Zeiger innerhalb der Struktur auf NULL festlegen.

Eine andere Situation, die zu einem Speicherplatz führt, umfasst konforme, abweichende und offene Arrays mit Zeigern. Wenn die Serveranwendung den Parameter ändert, der die Array Größe oder den übertragenen Bereich angibt, sodass Sie einen kleineren Wert darstellt, verwenden die stubwerte die kleineren Werte, um Arbeitsspeicher freizugeben. Die Array Elemente mit Indizes, die größer sind als der Size-Parameter, sind verwaist. Die Anwendung muss Elemente außerhalb des übertragenen Bereichs freigeben.

 

 