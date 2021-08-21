---
description: 'Die Ink Analysis-Bibliothek enthält vier Ebenen: Windows Forms, WPF, COM und die Basisebene. In diesem Abschnitt wird beschrieben, wann die einzelnen Ebenen verwendet werden.'
ms.assetid: bd190606-5bd8-4280-ba2b-267588904ed3
title: Verwendung der Ink Analysis-API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cdfada58868c7fe959f832e0c1243bc91a373fb0186d8deee2f9481d78a95714
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119032348"
---
# <a name="ink-analysis-api-usage"></a>Verwendung der Ink Analysis-API

Die Ink Analysis-Bibliothek enthält vier Ebenen: Windows Forms, WPF, COM und die Basisebene. In diesem Abschnitt wird beschrieben, wann die einzelnen Ebenen verwendet werden.

## <a name="ink-analysis-api-overview"></a>Übersicht über die Ink Analysis-API

Die Bibliotheken für die Ink-Analyse sind für die Verwendung in einer Vielzahl unterstützter Programmierumgebungen konzipiert. Es gibt vier grundlegende Ebenen, über die Ihre Anwendung die Ink-Analyse nutzen kann. Diese Ebenen sind:

-   Die Windows Forms-Ebene
-   Die WPF-Ebene
-   Die COM-Ebene
-   Die Basisebene

### <a name="windows-forms-applications"></a>Windows Forms-Anwendungen

Sie können die Ink Analysis-API in Ihrem verwalteten Projekt verwenden, indem Sie einen Verweis auf die folgenden Bibliotheken hinzufügen:

-   Microsoft.Ink.Analysis (Microsoft.Ink.Analysis.dll)
-   Ink Document Analysis Library (IACore.dll)

In Windows Forms-Anwendungen verwenden Sie höchstwahrscheinlich die Bibliotheken in Verbindung mit den standardmäßigen Tablet PC-Plattformobjekten, die sich in der Microsoft Tablet PC API v1.7-Assembly finden. Stellen Sie sicher, dass Sie auch über einen Verweis auf:

-   Microsoft Tablet PC API v1.7.2600.2180 (Microsoft.Ink.dll)

### <a name="windows-presentation-framework-applications"></a>Windows Presentation Framework-Anwendungen

Sie können die Ink Analysis-API in Ihrem WPF-Projekt verwenden, indem Sie einen Verweis auf die im System definierten Ink Analysis-Member hinzufügen. Windows. Der Ink-Namespace in der IAWinFX.dll Assembly. Diese Assembly wird vom SDK installiert.

### <a name="com-applications"></a>COM-Anwendungen

Com-Anwendungen ohne Automatisierung sollten die COM-Ebene der Ink Analysis-APIs verwenden.

Typspezifische [ContextNode-Objekte](/previous-versions/ms551996(v=vs.100)) wie [ParagraphNode,](/previous-versions/ms580136(v=vs.100)) [InkWordNode](/previous-versions/ms580133(v=vs.100))und andere werden in der COM-Ebene nicht verwendet. Stattdessen sollten Sie [**IContextNode::AddPropertyData auf**](icontextnode-addpropertydata.md) der [**IContextNode-Standardschnittstelle**](icontextnode.md) verwenden.

Sie müssen \# "IACom.h" enthalten. Da Sie wahrscheinlich die Bibliotheken zusammen mit dem Ink-Objekt der Tablet PC-Plattform verwenden, sollten Sie \# auch "msinkaut.h" verwenden.

### <a name="rts-and-other-applications"></a>RTS und andere Anwendungen

Die Basisebene der Ink-Analyse funktioniert anders als die anderen, da sie Punktdaten für die Analyse anstelle von [Stroke-Objekten](/previous-versions/ms552692(v=vs.100)) verwendet. Beispiele dafür, wo Sie direkt mit der Basisebene arbeiten würden, anstatt die Windows-Formulare oder COM-Ebenen zu verwenden, sind Anwendungen, die keine Tablet PC Platform Ink-Objekte der ersten Generation verwenden, oder Anwendungen, die [**die RealTimeStylus-APIs**](realtimestylus-class.md) zum Verwalten von Tablettstifteingaben anstelle der Tablet PC Platform [Ink-Objekte](/previous-versions/ms583670(v=vs.100)) verwenden.

## <a name="32-bit-support-only"></a>Nur 32-Bit-Unterstützung

Beachten Sie, dass die Bibliotheken für die Ink-Analyse nur in 32-Bit-Prozessen unterstützt werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Übersicht über die Ink-Analyse](ink-analysis-overview.md)
</dt> <dt>

[Referenz zur Ink-Analyse](ink-analysis-reference.md)
</dt> </dl>

 

 
