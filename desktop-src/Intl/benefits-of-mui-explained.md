---
description: Vorteile von MUI erläutert
ms.assetid: 5b9851e0-4354-4088-b099-0f5f5fac4a35
title: Vorteile von MUI erläutert
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1915e58e28ac9c7b3a43cc0ba217b8d56657c1b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041693"
---
# <a name="benefits-of-mui-explained"></a>Vorteile von MUI erläutert

-   [MUI-Vorteile für Entwickler](#mui-benefits-for-developers)
-   [MUI-Vorteile für Unternehmen](#mui-benefits-for-enterprises)
-   [Vorteile von MUI für OEMs](#mui-benefits-for-oems)

## <a name="mui-benefits-for-developers"></a>MUI-Vorteile für Entwickler

Es gibt viele Möglichkeiten, eine MUI-Lösung in-Anwendungen zu implementieren. jede Möglichkeit ist jedoch eine Variation einer von drei grundlegenden Methoden:

1.  Kompilieren einer Binärdatei (mit integrierten Ressourcen) für jede Sprache. Dies ist der *de-facto* -Standard für Legacy Anwendungen, da dies das primäre Modell ist, das von Standard Entwicklungs Tools wie Microsoft Visual Studio unterstützt wird. Dieses Modell erfordert mehrere Binärdateien für mehrere Sprachen und weist Einschränkungen hinsichtlich der Bereitstellung einzelner Images und mehrsprachige Szenarien auf. Beachten Sie, dass die mit diesem Modell entwickelten Anwendungen weiterhin unter Windows Vista funktionieren. diese Tools werden bereitgestellt, die Entwicklern dabei helfen, von diesem Modell zu dem moderneren Modell zu wechseln, das in der dritten Methode beschrieben wird.
2.  Die Verwendung einer sprach neutralen kernbinär Datei mit einer mehrsprachigen Ressourcen-DLL (Dynamic-Link Library). Dieses Modell ist definitiv MUI-freundlich, macht es jedoch schwierig, die Ressourcen Binärdateien zu aktualisieren, um neue Sprachen zu ermöglichen. Angenommen, Sie möchten neben Englisch, Französisch und Japanisch auch Deutsch unterstützen. Eine vollständige neue Ressourcen Binärdatei muss bereitgestellt und für die Benutzer bereitgestellt werden, die nicht unbedingt Deutsch benötigen.
3.  Die Verwendung einer sprach neutralen Kern Binärdatei mit einem Satz von Ressourcen-DLLs pro Sprache. Dies ist die Art und Weise, wie das Betriebssystem in Windows Vista implementiert wird. Entwicklern wird empfohlen, dieses Modell für Anwendungen zu verwenden, da es mehr als die vorherigen beiden Modelle bietet.

Vor der Windows Vista-Version machte das Fehlen integrierter Unterstützung für dieses letztere Modell die Übernahme schwierig. Dies hat sich jedoch geändert, und die Vorteile dieses Modells sind zahlreiche Vorteile, die das Modell für Ihre Anwendungen hervorragend gestalten:

-   Anwendungen können mehrsprachig gemacht werden und können sich auf die gleiche Weise wie Windows Vista Verhalten, was eine konsistente Anzeige Sprache für Benutzer bietet.
-   Flexibilität bei der Freigabe zusätzlicher Sprachen für eine Anwendung. Weitere Sprachen können unabhängig vom Kerncode freigegeben werden. Dies bedeutet, dass die Unterstützung für neue Sprachen im Laufe der Zeit nach Bedarf hinzugefügt werden kann.
-   Die Kosten werden bei der Erstellung und Wartung von sprach Releases reduziert.
-   OEMs und Unternehmen können problemlos Anwendungen in Ihr globalisiertes PC-Image integrieren – bereit für die Lieferung in verschiedenen Ländern.
-   Tools und Richtlinien, die Sie beim Migrieren Ihrer Anwendung zum Windows Vista MUI-Modell unterstützen, sind verfügbar. Insbesondere bietet MSDN eine [bedeutende Dokumentation](multilingual-user-interface.md) zu MUI.

## <a name="mui-benefits-for-enterprises"></a>MUI-Vorteile für Unternehmen

MUI bietet zwei wesentliche Vorteile für Unternehmen:

-   Installation mit einem einzelnen Image: mit MUI können Unternehmen das gleiche weltweite Image (oder eines beliebigen Teils davon) mit einer einzelnen Installation einführen, unterstützen und verwalten. Windows Vista erweitert das Rollout des Betriebssystems mit einem einzelnen Image, damit Geschäftsanwendungen auch als Teil des gleichen Images bereitgestellt werden können.
-   Unterstützung für mehrsprachige Desktops: Es können mehrere lokalisierte UI-Sprachpakete auf einem Desktop installiert werden. Dadurch können mehrere Benutzer einen einzelnen Desktop freigeben, während weiterhin ihre eigenen bevorzugten Benutzeroberflächen Sprachen verwendet werden. Dies gilt auch für öffentliche Computer, die eine gleichmäßige Behandlung für alle offiziell gesprochenen Sprachen benötigen (z. b. in Kanada und in der Europäischen Union), sowie für freigegebene Computer für Roamingbenutzer.

## <a name="mui-benefits-for-oems"></a>Vorteile von MUI für OEMs

Der größte Vorteil für OEMs ist die Installation von einem einzelnen Image, die MUI ermöglicht, da es möglich ist, Abbilder zu erstellen, die alle notwendigen Sprachen enthalten, um eine geografische Zone effektiv als Ziel festzustellen, und die Sprachauswahl für die Erstinstallation des Computers des Benutzers zu verzögern. Dies ermöglicht insbesondere eine effektivere Verwaltung des Inventars für OEMs.

Durch die Bereitstellung von MUI-Unterstützung für Anwendungen ermöglicht Windows Vista auch OEMs das Bereitstellen von Anwendungen zum Hinzufügen von Werten auf Ihren Images, während Sie von der Installation mit einem einzelnen Image profitieren, solange diese Anwendungen MUI-fähig sind.

 

 



