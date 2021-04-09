---
description: 'Es gibt vier Ebenen zur Handschrift Analyse Bibliothek: Windows Forms, WPF, com und die Basisebene. In diesem Abschnitt wird beschrieben, wann jede Ebene verwendet werden soll.'
ms.assetid: bd190606-5bd8-4280-ba2b-267588904ed3
title: Verwendung der frei Hand Analyse-API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24e291066d6cfd6ecdec319728b7394d730ba311
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958763"
---
# <a name="ink-analysis-api-usage"></a>Verwendung der frei Hand Analyse-API

Es gibt vier Ebenen zur Handschrift Analyse Bibliothek: Windows Forms, WPF, com und die Basisebene. In diesem Abschnitt wird beschrieben, wann jede Ebene verwendet werden soll.

## <a name="ink-analysis-api-overview"></a>Übersicht über die Ink Analysis-API

Die frei Hand Analyse Bibliotheken sind für die Verwendung in einer Vielzahl von unterstützten Programmierumgebungen konzipiert. Es gibt vier grundlegende Ebenen, in denen Ihre Anwendung die Handschrift Analyse nutzen kann. Diese Ebenen sind:

-   Die Windows Forms Ebene
-   Die WPF-Ebene
-   Die com-Ebene
-   Die Basisebene

### <a name="windows-forms-applications"></a>Windows Forms-Anwendungen

Sie können die frei Hand Analyse-API in Ihrem verwalteten Projekt verwenden, indem Sie einen Verweis auf die folgenden Bibliotheken hinzufügen:

-   Microsoft. Ink. Analysis (Microsoft.Ink.Analysis.dll)
-   Bibliothek für frei Hand Dokument Analyse (IACore.dll)

In Windows Forms Anwendungen verwenden Sie höchstwahrscheinlich die Bibliotheken in Verbindung mit den standardmäßigen Tablet PC-Platt Form Objekten, die in der Microsoft Tablet PC API v 1.7-Assembly gefunden werden. Stellen Sie sicher, dass Sie auch über einen Verweis auf Folgendes verfügen:

-   Microsoft Tablet PC API v 1.7.2600.2180 (Microsoft.Ink.dll)

### <a name="windows-presentation-framework-applications"></a>Windows Presentation Framework-Anwendungen

Sie können die frei Hand Analyse-API in Ihrem WPF-Projekt verwenden, indem Sie einen Verweis auf die im System. Windows. Ink-Namespace definierten Elemente der Ink-Analyse in der IAWinFX.dll-Assembly hinzufügen. Diese Assembly wird vom SDK installiert.

### <a name="com-applications"></a>COM-Anwendungen

Nicht-Automation-com-Anwendungen sollten die com-Ebene der frei Hand Analyse-APIs verwenden.

Typspezifische [ContextNode](/previous-versions/ms551996(v=vs.100)) -Objekte, z. b. " [ParagraphNode](/previous-versions/ms580136(v=vs.100))", " [InkWordNode](/previous-versions/ms580133(v=vs.100))" und andere, werden nicht in der com-Ebene verwendet. Stattdessen sollten Sie [**icontextnode:: AddPropertyData**](icontextnode-addpropertydata.md) auf der standardmäßigen [**icontextnode**](icontextnode.md) -Schnittstelle verwenden.

Sie müssen \# "iacom. h" einschließen. Wahrscheinlich verwenden Sie die Bibliotheken in Verbindung mit dem Tablet PC Platform Ink-Objekt. Daher sollten Sie auch \# "msink AUT. h" einschließen.

### <a name="rts-and-other-applications"></a>RTS und andere Anwendungen

Die Basisschicht der frei Hand Analyse funktioniert anders als die anderen, da Sie Punktdaten für die Analyse anstelle von [Stroke](/previous-versions/ms552692(v=vs.100)) -Objekten benötigt. Beispiele für die direkte Arbeit mit der Basisschicht anstelle der Windows Forms-oder com-Schichten sind Anwendungen, die keine Tablet PC Platform-Ink-Objekte der ersten Generation verwenden, oder Anwendungen, die die [**RealTimeStylus**](realtimestylus-class.md) -APIs verwenden, um Stift Eingaben zu verwalten, anstatt die Tablet PC Platform [Ink](/previous-versions/ms583670(v=vs.100)) -Objekte zu verwenden.

## <a name="32-bit-support-only"></a>nur 32-Bit-Unterstützung

Beachten Sie, dass die frei Hand Analyse Bibliotheken nur in 32-Bit-Prozessen unterstützt werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Übersicht über die Link Analyse](ink-analysis-overview.md)
</dt> <dt>

[Ink-Analyse Referenz](ink-analysis-reference.md)
</dt> </dl>

 

 
