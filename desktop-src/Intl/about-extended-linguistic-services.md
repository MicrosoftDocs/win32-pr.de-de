---
description: Erweiterte linguistische Dienste (Dynamic Link Library, ELS) werden als Dynamic Link Library (dll) implementiert, die eine Vielzahl von Funktionen für die linguistische Unterstützung für Text bereitstellt, den die Anwendung angibt.
ms.assetid: 23d4e42a-a5bb-467c-a8b9-6a57ae39daa0
title: Informationen zu erweiterten linguistischen Diensten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a6594fcfe67954a56cb09e239221b2b529d4d01
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349946"
---
# <a name="about-extended-linguistic-services"></a>Informationen zu erweiterten linguistischen Diensten

Erweiterte linguistische Dienste (Dynamic Link Library, ELS) werden als Dynamic Link Library (dll) implementiert, die eine Vielzahl von Funktionen für die linguistische Unterstützung für Text bereitstellt, den die Anwendung angibt. Die Technologie umfasst die Els-Plattform und Plug-Ins für mehrere vordefinierte linguistische Dienst Typen, auf die die Anwendung über die Plattform zugreifen kann.

> [!Note]  
> Das ELS-Modul wird automatisch mit Windows 7 und höher installiert.

 

## <a name="els-platform"></a>Els-Plattform

Die Els-Plattform ist die Schnittstelle zwischen Ihrer Anwendung und den Els-Diensten. Es bietet eine einfache Möglichkeit, mehrere Arten von linguistischen Funktionen über dieselbe API zu implementieren, sodass die Anwendung auf bestimmte Dienste zugreifen und diese verwenden kann. Weitere Informationen zur API finden Sie unter [Referenz zu erweiterten linguistischen Diensten.](extended-linguistic-services-reference.md)

> [!Note]  
> Wenn die Anwendung eine der Els-API-Funktionen aufruft, ordnet die Plattform Arbeitsspeicher und Ressourcen zu, die für die Kommunikation mit den Diensten erforderlich sind. Die Anwendung ist dafür verantwortlich, die Plattform erneut aufrufen zu können, um diese Ressourcen freizugeben.

 

Die Plattform wird im virtuellen Speicherbereich der Anwendung ausgeführt, und der gesamte zugeordnete Arbeitsspeicher ist Teil dieses Speicherplatzes. Daher muss Ihre Anwendung nur eine Verknüpfung mit der Els-Komponenten-DLL (Elscore.dll) herstellen, indem Sie eine Verknüpfung mit elscore. lib herstellen oder Elscore.dll dynamisch laden.

## <a name="els-services"></a>Els-Dienste

Für Windows 7 und höher unterstützt die Els-Plattform nur die folgenden vordefinierten Dienste.

-   [Microsoft-Sprachenerkennung](microsoft-language-detection.md)
-   [Microsoft-Skript Erkennung](microsoft-script-detection.md)
-   [Transliterations Dienste](transliteration-services.md)

> [!Note]  
> In zukünftigen Versionen von Els werden zusätzliche Dienste von Microsoft oder Dienstanbietern unterstützt.

 

Jeder Dienst ist einer Dienst Kategorie zugeordnet, die beschreibt, wie der Dienst funktioniert. Die Kategorie wird durch eine nicht lokalisierbare Zeichenfolge dargestellt. Sie wird von Anwendungen zum Auflisten der verfügbaren Dienste verwendet. Die aktuellen Dienst Kategorien lauten:

-   "Sprachenerkennung"
-   "Skript Erkennung"
-   Transliterations

Die Plattform listet die von der Anwendung angeforderten Dienste mithilfe von Dienst Metadaten auf. Eigenschaften wie der Dienst Globally Unique Identifier (GUID), unterstützte Eingabe-und Ausgabesprachen und Skripts sowie die Dienst Kategorie können von der Anwendung zum Auflisten der gewünschten Els-Dienste verwendet werden.

Jeder Els-Dienst wird als Plug-in implementiert, das von einer DLL unterstützt wird, die auf dem Betriebssystem installiert werden kann, damit die Els-Plattform diese erkennen und verwenden kann. Dienste können bei Bedarf Ihre eigenen subdienste verfügbar machen.

## <a name="main-els-operations"></a>Haupt Vorgänge von Els

In diesem Abschnitt werden die wichtigsten von der Els-Plattform unterstützten Vorgänge beschrieben. Die Plattform unterstützt sowohl synchrone als auch asynchrone Aufruf Modi. Der asynchrone Aufruf Modus verwendet einen Anwendungs Thread Pool, um Threads für Verarbeitungsanforderungen zu planen.

> [!Note]  
> Da die Plattform einen asynchronen Modus unterstützt, müssen Els-Dienste diese Art von Funktionalität nicht selbst implementieren.

 

### <a name="service-enumeration"></a>Dienst Enumeration

Die Els-Plattform lädt und verwaltet alle Els-Dienste, sodass der Vorgang für die Anwendung transparent ist. Die Anwendung listet die verfügbaren Dienste auf, indem [**mappinggetservices**](/windows/desktop/api/Elscore/nf-elscore-mappinggetservices)aufgerufen wird. Weitere Informationen zur Programmierung finden Sie unter Auflisten [und Freigeben von Diensten](enumerating-and-freeing-services.md).

> [!Note]  
> Aus Leistungsgründen wird empfohlen, dass die Anwendung die verfügbaren Dienste nur einmal aufzählt. Die Els-Plattform prüft die Dienste erneut auf die nächste Enumeration, um sicherzustellen, dass Ihre enumerationsergebnisse immer aktuell sind.

 

### <a name="text-recognition"></a>Text Erkennung

Nach der Dienst Enumeration Ruft die Anwendung die [**mappingrecognizetext**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext) -Funktion auf, um einen beliebigen Textbereich von Eingabetext dem Ausgabetext zuzuordnen. Ein Beispiel für die Texterkennung ist die Verwendung eines sprach Erkennungs Dienstanbieter, der ein Textsegment empfängt und seine wahrscheinlichste Sprache erkennt.

Nachdem der Dienst den Text erkannt hat, gibt [**mappingrecognizetext**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext) eine Zuordnung mit einer Eigenschaften Behälter Struktur aus, die mit den vom Dienst erzeugten Ausgabedaten und Eigenschaften aufgefüllt wurde. [**\_ \_**](/windows/desktop/api/Elscore/ns-elscore-mapping_property_bag) Um Speicher Verluste zu vermeiden, muss die Anwendung den Eigenschaften Behälter freigeben, indem Sie [**mappingfreepropertybag**](/windows/desktop/api/Elscore/nf-elscore-mappingfreepropertybag) für jedes Mal aufrufen, wenn [**mappingrecognizetext**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext) S OK zurückgibt \_ . In der Regel führt die Anwendung dies entweder aus, wenn Sie die Ausgabedaten verwendet, oder wenn die Ausgabedaten nicht mehr relevant sind, weil der Eingabebereich von Text geändert wurde (z. b. bearbeitet oder gelöscht). Wenn die Eigenschaften Sammlung freigegeben wird, gibt **mappingfrepropertybag** zurück.

Programmier Anweisungen für die Texterkennung werden bei der [Anforderung von Texterkennung](requesting-text-recognition.md)bereitgestellt.

### <a name="service-termination"></a>Dienst Beendigung

Wenn Ihre Anwendung keine Els-Dienste mehr erfordert, wird [**mappingfreeservices**](/windows/desktop/api/Elscore/nf-elscore-mappingfreeservices) aufgerufen, bevor Sie beendet wird. Weitere Informationen finden Sie unter Auflisten [und Freigeben von Diensten](enumerating-and-freeing-services.md).

### <a name="versioning"></a>Versionskontrolle

In zukünftigen Versionen von Els können die Els-Dienste aktualisiert werden. Die Anwendung kann die Versionsnummern der [**\_ zuordnungsdienstinfostruktur \_**](/windows/desktop/api/Elscore/ns-elscore-mapping_service_info) überprüfen, um Änderungen in den Diensten zu erkennen.

> [!Note]  
> Ihre Els-Anwendung sollte nicht die Annahme machen, dass unterschiedliche Versionen desselben Dienstanbieter genau die gleichen Ergebnisse abrufen können.

 

 

 



