---
title: Entwickeln der Schnittstelle
description: Eine RPC-Schnittstelle beschreibt die vom Serverprogramm implementierten Remote Funktionen.
ms.assetid: f0dfe9d1-fe84-461c-8684-147fbd0bdefe
keywords:
- Remote Prozedur Aufruf RPC, Tasks, entwickeln der Schnittstelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68b6f720bcd492e784ad07fe20e221ac54951680
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104102099"
---
# <a name="developing-the-interface"></a>Entwickeln der Schnittstelle

Eine RPC-Schnittstelle beschreibt die vom Serverprogramm implementierten Remote Funktionen. Die-Schnittstelle stellt sicher, dass der Client und der Server mit denselben Regeln kommunizieren, wenn der Client eine Remote Prozedur aufruft, die der Server anbietet. Eine Schnittstelle besteht aus einem Schnittstellennamen, einigen Attributen, optionalen Typ-oder Konstanten Definitionen und einem Satz von Prozedur Deklarationen. Jede Prozedur Deklaration muss den Namen der Prozedur, den Rückgabetyp und die Parameterliste enthalten.

Schnittstellen werden in der Microsoft Interface Definition Language (mittlerer l) definiert. Wenn Sie mit C oder C++ vertraut sind, erscheinen die Mittel l-Schnittstellendefinitionen recht unkompliziert. "Mittel l" ähnelt C und C++ in vielerlei Hinsicht.

Beim Entwickeln einer RPC-Anwendung wird ein Text-Editor verwendet, um die Schnittstelle zu definieren und in einer Textdatei mit der Erweiterung IDL zu speichern. Weitere Informationen finden Sie in [den IDL-und ACF-Dateien](the-idl-and-acf-files.md). Der-compilercompiler generiert eine Header Datei, die das Programm in den Quelldateien für Client und Server enthält. Der mittlerer l-Compiler generiert außerdem zwei C-Quelldateien. Sie kompilieren und verknüpfen einen dieser Dateien mit Ihrem Client Programm und dem anderen mit dem Serverprogramm. Diese beiden C-Quelldateien sind die Client-und Serverstub. Eine Übersicht über die Client-und serverstubvorgänge finden Sie unter [Funktionsweise von RPC](how-rpc-works.md). Eine Übersicht über den-Mittell-Compiler finden Sie unter [Kompilieren einer Mittel l-Datei](using-midl.md).

Standardmäßig haben die Client-und Serverstubs denselben Namen, was zu Problemen führen kann, wenn der Client mit dem Serverstub verknüpft wird (oder umgekehrt). Die Verwendung der Option "Mittel l [**/prefix**](/windows/desktop/Midl/-prefix) " verhindert, dass dieser häufige Fehler auftritt.

Die folgende Abbildung zeigt den Prozess der Erstellung einer Schnittstelle.

![durch die Erstellung von Client-und serverstubstuptem mit der Option/prefix werden Probleme bei der](images/idldev.png)

Es ist möglich, dass Sie auch eine Anwendungs Konfigurationsdatei (ACF) für die Eingabe an den Mittelwert Compiler angeben müssen. Weitere Informationen zu Anwendungs Konfigurationsdateien finden Sie in [den IDL-und ACF-Dateien](the-idl-and-acf-files.md).

Zusätzlich zum Mittelwert des compl-Compilers müssen Sie das Hilfsprogramm uuidgen verwenden, um einen universellen eindeutigen Bezeichner (UUID, austauschbar mit dem Begriff GUID) zu generieren. Dieser Abschnitt enthält Informationen zu diesen beiden Tools, die in die folgenden Themen unterteilt sind:

-   [Erstellen von Schnittstellen-UUIDs](generating-interface-uuids.md)
-   [Verwenden von Mittel l](using-midl.md)

 

 