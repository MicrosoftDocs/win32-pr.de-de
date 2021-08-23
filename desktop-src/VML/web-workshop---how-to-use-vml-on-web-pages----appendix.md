---
title: Anhang (VML)
description: In diesem Thema wird VML beschrieben, ein Feature, das ab Windows Internet Explorer 9 als veraltet gilt.
ms.assetid: e18e9388-d8b6-4eee-b4f1-3948830f7986
keywords:
- Web workshop,namespaces
- Web-Workshop, Verhaltensstile
- Entwerfen von Webseiten, Namespaces
- Entwerfen von Webseiten, Verhaltensstilen
- Vector Markup Language (VML),Namespaces
- VML (Vector Markup Language),namespaces
- Vektorgrafiken, Namespaces
- Vector Markup Language (VML), Verhaltensstile
- VML (Vector Markup Language),Verhaltensstile
- Vektorgrafiken, Verhaltensstile
- VGX.DLL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 640de79138adcc345d4352ead814195007b88e0714a0f89816819d545e6e1ef6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119512610"
---
# <a name="appendix-vml"></a>Anhang (VML)

In diesem Thema wird VML beschrieben, ein Feature, das ab Windows Internet Explorer 9 als veraltet gilt. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Seit Dezember 2011 wurde dieses Thema archiviert. Daher wird sie nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/) Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie unter [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Damit die Browser wissen, wie Daten an einen VML-spezifischen Prozessor übergeben werden, müssen Sie einige Informationen wie Namespaces und Verhaltensstile eingeben. Anschließend können Sie VML verwenden, um Grafiken in der `<BODY>` Region einzugeben.

In diesem Thema:

-   [Namespaces](#namespaces)
-   [Verhaltensstile](#behavior-styles)

## <a name="namespaces"></a>Namespaces

Ein XML-Mechanismus gibt den Namespace an, aus dem ein Element stammt. Wenn Sie von der Analyse in HTML zur Analyse in XML wechseln, gibt dieser Mechanismus den Schalter in HTML an.

Fragen Sie den Automaten Ihres VML-Prozessors, welche Informationen für den XML-Namespace erforderlich sind.

Wenn Sie Microsoft Internet Explorer zum Rendern von VML verwenden, geben Sie immer die folgende Zeile in das `<HTML>` Tag ein:


```HTML
<html xmlns:v="urn:schemas-microsoft-com:vml">
```



Diese Informationen informieren Internet Explorer, beim Analysieren eines XML-Tags mit einem Präfix zum Namespace "urn:schemas-microsoft-com:vml" zu wechseln `v:` und die resultierenden Daten an den VML-Prozessor zu übergeben.

[![Zurück zum Anfang ](images/top.gif) Zurück zum Anfang](#top)

## <a name="behavior-styles"></a>Verhaltensstile

VML wird in Microsoft Internet Explorer als Standardverhalten definiert.

Geben Sie zum Rendern von VML immer die folgenden Zeilen in der `<HEAD>` Region ein:


```HTML
<style>
v\:* { behavior: url(#default#VML); display:inline-block}
</style>
```



VML wird in Internet Explorer über VGX.DLL implementiert. Wenn die Erstinstallation des Browsers kein VML-Verhalten enthält, müssen Sie es möglicherweise als Option hinzufügen. Sie müssen kein `<object>` Tag hinzufügen.

 

 
