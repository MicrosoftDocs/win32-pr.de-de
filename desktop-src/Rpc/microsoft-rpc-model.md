---
title: Das RPC-Modell
description: Remote Procedure Call (RPC) für die Programmiersprachen C und C++ wurde entwickelt, um die Anforderungen von Entwicklern zu erfüllen, die an der nächsten Generation von Software für Windows Betriebssysteme arbeiten.
ms.assetid: ebab41a5-e841-4e0f-8acd-d0aab94f01c1
keywords:
- Remoteprozeduraufruf RPC , beschrieben, das RPC-Modell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0dc4c21a9fbbff24f4aafe9bad67186b65f4e3411b507d07953e29f806c6ff73
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120019710"
---
# <a name="the-rpc-model"></a>Das RPC-Modell

Remote Procedure Call (RPC) für die Programmiersprachen C und C++ wurde entwickelt, um die Anforderungen von Entwicklern zu erfüllen, die an der nächsten Generation von Software für Windows Betriebssysteme arbeiten.

RPC ist ein leistungsstarker, stabiler, effizienter und sicherer Mechanismus für die prozessübergreifende Kommunikation (InterProcess Communication, IPC), der den Datenaustausch und den Aufruf von Funktionen ermöglicht, die sich in einem anderen Prozess befinden. Dieser unterschiedliche Prozess kann sich auf demselben Computer, im lokalen Netzwerk oder über das Internet befinden. In diesem Abschnitt werden das RPC-Programmiermodell und das Modell für verteilte Systeme erläutert, die mit RPC implementiert werden können.

RPC unterstützt 64-Bit-Windows vollständig. Es gibt drei Arten von Prozessen: native 32-Bit-Prozesse, native 64-Bit-Prozesse und 32-Bit-Prozesse, die unter dem 32-Bit-Prozessemulator auf einem 64-Bit-System ausgeführt werden (häufig als WOW64-Prozesse bezeichnet). Weitere Informationen zu WOW64 finden Sie unter [Ausführen von 32-Bit-Anwendungen.](/windows/desktop/WinProg64/running-32-bit-applications) Mit RPC können Entwickler transparent zwischen verschiedenen Prozesstypen kommunizieren. RPC verwaltet Prozessunterschiede automatisch im Hintergrund.

RPC wurde ursprünglich als Erweiterung für OSF RPC entwickelt. Mit Ausnahme einiger erweiterter Features ist RPC mit den Implementierungen von OSF RPC anderer Anbieter interoperabel.

Dieser Abschnitt bietet auch eine Übersicht über RPC-Komponenten und deren Betrieb. Die Informationen werden in den folgenden Themen vorgestellt:

-   [Das Programmiermodell](the-programming-model.md)
-   [Das Modell für verteilte Systeme](the-model-for-distributed-systems.md)
-   [Funktionsweise von RPC](how-rpc-works.md)
-   [Microsoft RPC-Komponenten](microsoft-rpc-components.md)

 

 