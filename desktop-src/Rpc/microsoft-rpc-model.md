---
title: Das RPC-Modell
description: Der Remote Prozedur Aufruf (RPC) für die Programmiersprachen C und C++ wurde entwickelt, um die Anforderungen von Entwicklern zu erfüllen, die an der nächsten Generation von Software für Windows-Betriebssysteme arbeiten.
ms.assetid: ebab41a5-e841-4e0f-8acd-d0aab94f01c1
keywords:
- Remote Prozedur Aufruf RPC, beschrieben, das RPC-Modell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e72048b12329133fcc8ce4ee82bce266ed29162
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729416"
---
# <a name="the-rpc-model"></a>Das RPC-Modell

Der Remote Prozedur Aufruf (RPC) für die Programmiersprachen C und C++ wurde entwickelt, um die Anforderungen von Entwicklern zu erfüllen, die an der nächsten Generation von Software für Windows-Betriebssysteme arbeiten.

RPC ist ein leistungsfähiger, stabiler, effizienter und sicherer Prozess für die prozessübergreifende Kommunikation (prozessübergreifende Communication, IPC), der den Datenaustausch und den Aufruf von Funktionen in einem anderen Prozess ermöglicht. Der andere Prozess kann sich auf demselben Computer, im lokalen Netzwerk oder über das Internet befinden. In diesem Abschnitt werden das RPC-Programmiermodell und das Modell für verteilte Systeme erläutert, die mithilfe von RPC implementiert werden können.

RPC unterstützt 64-Bit-Windows vollständig. Es gibt drei Arten von Prozessen: systemeigene 32-Bit-Prozesse, native 64-Bit-Prozesse und 32-Bit-Prozesse, die unter dem 32-Bit-Prozess Emulator auf einem 64-Bit-System ausgeführt werden (häufig als WOW64 Processes bezeichnet). Weitere Informationen zu WOW64 finden Sie unter [Ausführen von 32-Bit-Anwendungen](/windows/desktop/WinProg64/running-32-bit-applications). Mithilfe von RPC können Entwickler zwischen verschiedenen Prozess Typen transparent kommunizieren. RPC verwaltet Prozess Unterschiede automatisch im Hintergrund.

RPC wurde anfänglich als Erweiterung für OSF RPC entwickelt. Mit Ausnahme einiger erweiterter Features ist RPC mit den Implementierungen von OSF RPC anderer Hersteller interoperabel.

Dieser Abschnitt bietet auch eine Übersicht über die RPC-Komponenten und deren Betrieb. Die Informationen finden Sie in den folgenden Themen:

-   [Das Programmiermodell](the-programming-model.md)
-   [Das Modell für verteilte Systeme](the-model-for-distributed-systems.md)
-   [Funktionsweise von RPC](how-rpc-works.md)
-   [Microsoft RPC-Komponenten](microsoft-rpc-components.md)

 

 