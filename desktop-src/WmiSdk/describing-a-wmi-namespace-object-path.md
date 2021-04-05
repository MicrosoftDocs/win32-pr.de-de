---
description: Ein Namespace Objekt Pfad beschreibt den Speicherort eines bestimmten Namespaces auf einem Server. Ein Namespace Objekt Pfad enthält Server-und Namespace Elemente und wird entweder mit vorwärts-oder rückwärts Schrägstrichen formatiert.
ms.assetid: 6d8da19e-0914-4267-870e-c203176b895e
ms.tgt_platform: multiple
title: Beschreiben eines Objekt Pfads für den WMI-Namespace
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 586104a1c193f1c229b0fbb27437d22e3686585b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104042058"
---
# <a name="describing-a-wmi-namespace-object-path"></a>Beschreiben eines Objekt Pfads für den WMI-Namespace

Ein Namespace Objekt Pfad beschreibt den Speicherort eines bestimmten Namespaces auf einem Server. Ein Namespace Objekt Pfad enthält Server-und Namespace Elemente und wird entweder mit vorwärts-oder rückwärts Schrägstrichen formatiert.

Das Server-Element gibt den Netzwerknamen des Computers an, auf dem der Namespace gehostet wird, wie im folgenden Beispiel gezeigt.

``` syntax
\\Server\Namespace
```

\- oder -

``` syntax
//Server/Namespace
```

Wenn der Server der lokale Computer ist, verwenden Sie einen einzelnen Punkt anstelle des Server namens, wie im folgenden Beispiel gezeigt.

``` syntax
\\.\Namespace
```

Das Namespace-Element gibt einen beliebigen gültigen Namespace an. Ein Namespace wird durch eine hierarchische Zeichenfolge dargestellt, die Elemente enthält, die durch einzelne umgekehrte Schrägstriche (z. b. root cimv2) getrennt sind \\ . Sie können keine Schrägstriche innerhalb von Namespace Namen verwenden.

 

 



