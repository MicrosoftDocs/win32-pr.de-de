---
title: Die IDL- und ACF-Dateien
description: Die Syntax der Microsoft Interface Definition Language (MIDL) basiert auf der Syntax der Programmiersprache C. Wenn ein Sprachkonzept in dieser Beschreibung von MIDL nicht vollständig definiert ist, wird die C-Sprachdefinition dieses Begriffs impliziert.
ms.assetid: f99f5934-750d-4c30-9970-803a891cacb7
keywords:
- RPC-Remoteprozeduraufruf , beschriebene IDL- und ACF-Dateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 788756c6762575d2366950f1b6412a76c03d14518acb1707dfdaf109ba2b5fc6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120017100"
---
# <a name="the-idl-and-acf-files"></a>Die IDL- und ACF-Dateien

Die Syntax der Microsoft Interface Definition Language (MIDL) basiert auf der Syntax der Programmiersprache C. Wenn ein Sprachkonzept in dieser Beschreibung von MIDL nicht vollständig definiert ist, wird die C-Sprachdefinition dieses Begriffs impliziert.

Der MIDL-Entwurf gibt zwei unterschiedliche Dateien an: die IDL-Datei (Interface Definition Language) und die Anwendungskonfigurationsdatei (Application Configuration File, ACF). Diese Dateien enthalten Attribute, die die Generierung der Stubdateien in C-Sprache steuern, die den Remoteprozeduraufruf (RPC) verwalten. Die IDL-Datei enthält eine Beschreibung der Schnittstelle zwischen dem Client und den Serverprogrammen. RPC-Anwendungen verwenden die ACF-Datei, um die Merkmale der Schnittstelle zu beschreiben, die spezifisch für die Hardware und das Betriebssystem sind, die eine bestimmte Betriebssystemumgebung darstellen. Der Zweck der Unterteilung dieser Informationen in zwei Dateien besteht im Trennen der Softwareschnittstelle von Merkmalen, die sich nur auf die Betriebsumgebung auswirken.

Die IDL-Datei gibt einen Netzwerkvertrag zwischen Client und Server an, d.&a; die IDL-Datei gibt an, was zwischen dem Client und dem Server übertragen wird. Wenn diese Informationen von den Informationen über die Betriebsumgebung getrennt bleiben, wird die IDL-Datei auf andere Umgebungen portierbar. Die IDL-Datei besteht aus zwei Teilen: einem [Schnittstellenheader](the-idl-interface-header.md) und einem [Schnittstellenkörper.](the-idl-interface-body.md)

Der ACF gibt Attribute an, die sich nicht auf den Netzwerkvertrag, sondern nur auf die lokale Leistung auswirken. Mit Microsoft RPC können Sie die Attribute ACF und IDL in einer einzelnen IDL-Datei kombinieren. Sie können auch mehrere Schnittstellen in einer einzelnen IDL-Datei (und deren ACF) kombinieren.

In diesem Abschnitt werden die Attribute zusammengefasst, die in den IDL- und ACF-Dateien angegeben sind. Es soll nur eine Übersicht bereitstellen. Ausführlichere Informationen finden Sie in der [MIDL-Sprachreferenz](/windows/desktop/Midl/midl-language-reference)und in der [MIDLCommand-Line Referenz.](/windows/desktop/Midl/midl-command-line-reference) Die Diskussion in diesem Abschnitt wird in den folgenden Themen behandelt:

-   [Die IDL-Datei (Interface Definition Language)](the-interface-definition-language-idl-file.md)
-   [Die Anwendungskonfigurationsdatei (Application Configuration File, ACF)](the-application-configuration-file-acf-.md)
-   [MIDL-Compilerausgabe](midl-compiler-output.md)

 

 