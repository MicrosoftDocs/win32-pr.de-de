---
title: Entwickeln der Schnittstelle
description: Eine RPC-Schnittstelle beschreibt die Remotefunktionen, die vom Serverprogramm implementiert werden.
ms.assetid: f0dfe9d1-fe84-461c-8684-147fbd0bdefe
keywords:
- Remoteprozeduraufruf RPC , Tasks, Entwickeln der Schnittstelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c23829dcf143f63e791984e51194686d193d69cd575fadbc0e29c13a6f2279df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118930602"
---
# <a name="developing-the-interface"></a>Entwickeln der Schnittstelle

Eine RPC-Schnittstelle beschreibt die Remotefunktionen, die vom Serverprogramm implementiert werden. Die Schnittstelle stellt sicher, dass Client und Server mit denselben Regeln kommunizieren, wenn der Client eine Remoteprozedur aufruft, die der Server anbietet. Eine Schnittstelle besteht aus einem Schnittstellennamen, einigen Attributen, optionalen Typ- oder Konstantendefinitionen und einer Reihe von Prozedurdeklarationen. Jede Prozedurdeklaration muss einen Prozedurnamen, einen Rückgabetyp und eine Parameterliste enthalten.

Schnittstellen werden im Microsoft Interface Definition Language (MIDL) definiert. Wenn Sie mit C oder C++ vertraut sind, erscheinen MIDL-Schnittstellendefinitionen ziemlich unkompliziert. MIDL ähnelt in vielerlei Hinsicht C und C++.

Beim Entwickeln einer RPC-Anwendung wird ein Text-Editor verwendet, um die Schnittstelle zu definieren und in einer Textdatei mit der Erweiterung .idl zu speichern. Weitere Informationen finden Sie unter [Die IDL- und ACF-Dateien.](the-idl-and-acf-files.md) Der MIDL-Compiler generiert eine Headerdatei, die Ihr Programm in die Client- und Serverquelldateien einschließt. Der MIDL-Compiler generiert auch zwei C-Quelldateien. Sie kompilieren und verknüpfen eine dieser Dateien mit Ihrem Clientprogramm und die andere mit Ihrem Serverprogramm. Diese beiden C-Quelldateien sind die Client- und Serverstubs. Eine Übersicht über die Client- und Serverstubs finden Sie unter Funktionsweise von [RPC.](how-rpc-works.md) Eine Übersicht über den MIDL-Compiler finden Sie unter [Kompilieren einer MIDL-Datei.](using-midl.md)

Standardmäßig haben der Client- und der Serverstub den gleichen Namen, was zu Problemen führen kann, wenn der Client mit dem Serverstub verknüpft ist oder umgekehrt. Die Verwendung der MIDL-Option [**/prefix**](/windows/desktop/Midl/-prefix) verhindert, dass dieser häufige Fehler auftritt.

Die folgende Abbildung zeigt den Prozess der Erstellung einer Schnittstelle.

![Erstellen von Client- und Serverstubs mit der Option /prefix verhindert versehentliche Kompilierungsprobleme.](images/idldev.png)

Es ist möglich, dass Sie auch eine Anwendungskonfigurationsdatei (Application Configuration File, ACF) für die Eingabe an den MIDL-Compiler angeben müssen. Weitere Informationen zu Anwendungskonfigurationsdateien finden Sie unter [Die IDL- und ACF-Dateien.](the-idl-and-acf-files.md)

Zusätzlich zum MIDL-Compiler müssen Sie in der Regel das Hilfsprogramm Uuidgen verwenden, um einen universellen eindeutigen Bezeichner (Universal Unique Identifier, UUID, austauschbar mit dem Begriff GUID) zu generieren. Dieser Abschnitt enthält Informationen zu beiden Tools, unterteilt in die folgenden Themen:

-   [Generieren von Schnittstellen-UUIDs](generating-interface-uuids.md)
-   [Verwenden von MIDL](using-midl.md)

 

 