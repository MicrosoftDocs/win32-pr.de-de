---
title: Die IDL-und ACF-Dateien
description: Die Syntax des Microsoft Interface Definition Language (mittlerer l) basiert auf der Syntax der Programmiersprache C. Wenn ein sprach Konzept in dieser Beschreibung von "Mittel l" nicht vollständig definiert ist, wird die C-Sprachdefinition dieses Begriffs impliziert.
ms.assetid: f99f5934-750d-4c30-9970-803a891cacb7
keywords:
- Remote Prozedur Aufruf RPC, beschrieben, IDL-und ACF-Dateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9f7f739e50fd4e04ae35a11adcbbc936cd3cb36
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103948940"
---
# <a name="the-idl-and-acf-files"></a>Die IDL-und ACF-Dateien

Die Syntax des Microsoft Interface Definition Language (mittlerer l) basiert auf der Syntax der Programmiersprache C. Wenn ein sprach Konzept in dieser Beschreibung von "Mittel l" nicht vollständig definiert ist, wird die C-Sprachdefinition dieses Begriffs impliziert.

Das Mittel l-Design gibt zwei unterschiedliche Dateien an: die IDL-Datei (Interface Definition Language) und die Anwendungs Konfigurationsdatei (ACF). Diese Dateien enthalten Attribute, die die Generierung der C-Sprachen-Stub-Dateien leiten, die den Remote Prozedur Aufruf (RPC) verwalten. Die IDL-Datei enthält eine Beschreibung der Schnittstelle zwischen dem Client und den Serverprogrammen. RPC-Anwendungen verwenden die ACF-Datei, um die Eigenschaften der Benutzeroberfläche zu beschreiben, die für die Hardware und das betriebssystemspezifisch sind, die eine bestimmte Betriebsumgebung bilden. Der Zweck der Aufteilung dieser Informationen in zwei Dateien besteht darin, die Softwareschnittstelle von Merkmalen getrennt zu halten, die sich nur auf die Betriebsumgebung auswirken.

Die IDL-Datei gibt einen Netzwerk Vertrag zwischen Client und Server an – d. h. die IDL-Datei gibt an, was zwischen Client und Server übertragen wird. Wenn diese Informationen von den Informationen zur Betriebsumgebung abweichen, wird die IDL-Datei in andere Umgebungen portierbar. Die IDL-Datei besteht aus zwei Teilen: einem [Schnittstellen Header](the-idl-interface-header.md) und einem [Schnittstellen Text](the-idl-interface-body.md).

Die ACF gibt Attribute an, die sich nur auf die lokale Leistung und nicht auf den Netzwerk Vertrag auswirken. Microsoft RPC ermöglicht Ihnen das Kombinieren der ACF-und IDL-Attribute in einer einzelnen IDL-Datei. Sie können auch mehrere Schnittstellen in einer einzelnen IDL-Datei (und ihrer ACF) kombinieren.

In diesem Abschnitt werden die Attribute zusammengefasst, die in den IDL-und ACF-Dateien angegeben sind. Es soll nur eine Übersicht bereitgestellt werden. Ausführlichere Informationen finden Sie in der Referenz zur [Mittel l-Sprache](/windows/desktop/Midl/midl-language-reference)und in der [Command-Line-Referenz](/windows/desktop/Midl/midl-command-line-reference). Die Erörterung dieses Abschnitts finden Sie in den folgenden Themen:

-   [Die IDL-Datei (Interface Definition Language)](the-interface-definition-language-idl-file.md)
-   [Die Anwendungs Konfigurationsdatei (ACF)](the-application-configuration-file-acf-.md)
-   [Mittel l-Compilerausgabe](midl-compiler-output.md)

 

 