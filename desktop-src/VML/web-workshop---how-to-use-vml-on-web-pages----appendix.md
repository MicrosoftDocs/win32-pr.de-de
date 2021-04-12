---
title: Anhang (VML)
description: In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.
ms.assetid: e18e9388-d8b6-4eee-b4f1-3948830f7986
keywords:
- Webworkshop, Namespaces
- Webworkshop, Verhaltens Stile
- Entwerfen von Webseiten, Namespaces
- Entwerfen von Webseiten, Verhaltens Stilen
- Vector Markup Language (VML), Namespaces
- VML (Vector Markup Language), Namespaces
- Vektorgrafiken, Namespaces
- Vector Markup Language (VML), Verhaltens Stile
- VML (Vector Markup Language), Verhaltens Stile
- Vektorgrafiken, Verhaltens Stile
- VGX.DLL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7d4e7a6a7e44671b7ee835eea263d9ce36a27d8
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104391423"
---
# <a name="appendix-vml"></a>Anhang (VML)

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Wenn Sie den Browsern mitteilen möchten, wie Daten an einen VML-spezifischen Prozessor übergeben werden, müssen Sie einige Informationen eingeben, z. b. Namespaces und Verhaltens Stile. Anschließend können Sie mit VML Grafiken in der Region eingeben `<BODY>` .

In diesem Thema:

-   [Namespaces](#namespaces)
-   [Verhaltens Stile](#behavior-styles)

## <a name="namespaces"></a>Namespaces

Ein XML-Mechanismus gibt den Namespace an, aus dem ein Element stammt. Wenn Sie von der XML-Datei zur XML-Verarbeitung wechseln, gibt dieser Mechanismus den Switch innerhalb von HTML an.

Fragen Sie den Hersteller des VML-Prozessors, welche Informationen für den XML-Namespace erforderlich sind.

Wenn Sie Microsoft Internet Explorer zum Rendering von VML verwenden, geben Sie immer die folgende Zeile im- `<HTML>` Tag ein:


```HTML
<html xmlns:v="urn:schemas-microsoft-com:vml">
```



Mit diesen Informationen wird Internet Explorer aufgefordert, zum Namespace "urn: Schemas-Microsoft-com: VML" zu wechseln, wenn ein XML-Tag mit einem Präfix `v:` und die resultierenden Daten an den VML-Prozessor übergeben werden.

[![zurück ](images/top.gif) zum Anfang](#top)

## <a name="behavior-styles"></a>Verhaltens Stile

VML ist in Microsoft Internet Explorer als Standardverhalten definiert.

Geben Sie zum Rendering von VML immer die folgenden Zeilen in der `<HEAD>` Region ein:


```HTML
<style>
v\:* { behavior: url(#default#VML); display:inline-block}
</style>
```



VML wird in Internet Explorer über VGX.DLL implementiert. Wenn die anfängliche Installation des Browsers kein VML-Verhalten enthielt, müssen Sie es möglicherweise als Option hinzufügen. Sie müssen kein-Tag hinzufügen `<object>` .

 

 
