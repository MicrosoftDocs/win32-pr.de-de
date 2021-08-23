---
title: Microsoft Interface Definition Language
description: Die Microsoft Interface Definition Language (MIDL) definiert Schnittstellen zwischen Client- und Serverprogrammen.
ms.assetid: 5ed1ff94-bbcb-4c6e-83aa-63d24eb84859
keywords:
- MIDL MIDL
- MIDL MIDL , (siehe Microsoft Interface Definition Language MIDL )
- Microsoft Interface Definition Language MIDL
- Microsoft Interface Definition Language MIDL , Startseite
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9062d5b2af18f7c3aa5ad57a4cb8f606cccc43333e4eff17d3518f72b7a064a4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119534970"
---
# <a name="microsoft-interface-definition-language"></a>Microsoft Interface Definition Language

## <a name="purpose"></a>Zweck

Die Microsoft Interface Definition Language (MIDL) definiert Schnittstellen zwischen Client- und Serverprogrammen. Microsoft enthält den MIDL-Compiler mit dem Platform Software Development Kit (SDK), damit Entwickler die IDL-Dateien (Interface Definition Language) und Anwendungskonfigurationsdateien (Application Configuration Files, ACF) erstellen können, die für RPC-Schnittstellen (Remote Procedure Call) und COM/DCOM-Schnittstellen erforderlich sind. MIDL unterstützt auch die Generierung von Typbibliotheken für die OLE-Automatisierung.

## <a name="where-applicable"></a>Anwendungsbereich

MIDL kann in allen Client-/Serveranwendungen basierend auf Windows verwendet werden. Sie kann auch verwendet werden, um Client- und Serverprogramme für heterogene Netzwerkumgebungen zu erstellen, die Betriebssysteme wie Unix und Apple enthalten. Microsoft unterstützt den DCE-Standard Open Group (ehemals Open Software Foundation) für die RPC-Interoperabilität.

## <a name="developer-audience"></a>Entwicklergruppe

Wenn Sie MIDL mit RPC verwenden, müssen Sie mit der C/C++-Programmierung und dem RPC-Paradigma vertraut sein. Wenn Sie MIDL mit COM verwenden, müssen Sie mit der C++-Programmierung und dem RPC-Paradigma vertraut sein, da es für COM gilt. Alternativ ist auch Vertrautheit mit der Ole Automation-Modellskripterstellung und Typbibliotheken erforderlich.

## <a name="run-time-requirements"></a>Laufzeitanforderungen

Die entsprechenden Laufzeitbibliotheken für die Verwendung von MIDL sind in Windows. Der MIDL-Compiler und die Komponenten der RPC-Entwicklungsumgebung werden installiert, wenn Sie das Windows installieren. Weitere Informationen finden Sie unter [Verwenden des MIDL-Compilers](using-the-midl-compiler-2.md) und [Installieren der RPC-Programmierumgebung.](/windows/desktop/Rpc/installing-the-rpc-programming-environment)

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                               | Beschreibung                                                                        |
|-----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [Übersicht](about-this-guide-2.md)<br/>                                                       | Allgemeine Informationen zu MIDL und dem MIDL-Compiler.<br/>                   |
| [Verwenden des MIDL-Compilers](using-the-midl-compiler-2.md)<br/>                                 | Informationen zur Verwendung des MIDL-Kompilierungs- zum Generieren von RPC-Stubs.<br/>       |
| [Schnittstellendefinitionen und Typbibliotheken](interface-definitions-and-type-libraries.md)<br/> | Dokumentation zu RPC-spezifischen Schnittstellendefinitionen und Typbibliotheken.<br/> |
| [MIDLCommand-Line Referenz](midl-command-line-reference.md)<br/>                           | Dokumentation der MIDL-Compilerbefehlszeilenschalter.<br/>               |
| [MIDL-Sprachreferenz](midl-language-reference.md)<br/>                                   | Die MIDL-Compilersprachreferenz.<br/>                                   |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Remoteprozeduraufruf (RPC)](/windows/desktop/Rpc/rpc-start-page)
</dt> </dl>

 

