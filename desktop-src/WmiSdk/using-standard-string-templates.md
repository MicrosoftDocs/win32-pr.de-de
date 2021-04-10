---
description: Mehrere Consumer, z. b. der aktive Skript Ereignisconsumer oder der Befehlszeilen-Ereignisconsumer, verfügen über Zeichen folgen Eigenschaften mit dem Vorlagen Qualifizierer.
ms.assetid: d734c226-e160-4834-a5e8-62390905dfde
ms.tgt_platform: multiple
title: Verwenden von Standard mäßigen Zeichen folgen Vorlagen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffc95f4b2b9b9f22e993d1de9cc8b35915918643
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866867"
---
# <a name="using-standard-string-templates"></a>Verwenden von Standard mäßigen Zeichen folgen Vorlagen

Mehrere Consumer, z. b. der aktive Skript Ereignisconsumer oder der Befehlszeilen-Ereignisconsumer, verfügen über Zeichen folgen Eigenschaften mit dem **Vorlagen** Qualifizierer. Diese Eigenschaften verwenden standardmäßige Zeichen folgen Vorlagen, um eine Zeichenfolge zu erstellen, die teilweise von der consumerinstanz und teilweise von einem Ereignis konfiguriert wird. Die Struktur einer Standard Zeichen folgen Vorlage ähnelt der Spezifikation der Microsoft Windows-Umgebungsvariablen.

In der folgenden Liste sind einige Beispiele für die Vorlagen Sprache aufgeführt:

-   Die Zeichenfolge "Text hier" erzeugt immer die Zeichenfolge "Text hier".
-   "% Cpuausnutzung%" erzeugt immer den Wert der **cpunutzungseigenschaft** des übermittelten Ereignisses. Wenn die Eigenschaft keine Zeichenfolge ist, wird Sie in eine Zeichenfolge konvertiert. Beispiel: "90" oder "true".
-   "Die CPU-Auslastung dieses Prozessors ist zu diesem Zeitpunkt% cpuausnutzung%." bettet den Wert der **cpunutzungseigenschaft** des Ereignisses in die Zeichenfolge ein und erzeugt so etwa Folgendes: "die CPU-Auslastung dieses Prozessors ist 90.
-   "% TargetInstance. cpuauslastungs%" Ruft den Wert der **cpunutzungseigenschaft** in der eingebetteten Instanz der **TargetInstance** -Eigenschaft ab.
-   "%%" erzeugt ein einzelnes%-Zeichen.
-   Wenn es sich bei der abgerufenen Eigenschaft um ein Array handelt, wird das gesamte Array im folgenden Format erstellt: "(1, 5, 10, 1024)". Wenn nur ein-Element im-Array vorhanden ist, werden die Klammern ausgelassen. Wenn keine Elemente im Array vorhanden sind, wird "()" erstellt.
-   Wenn eine Eigenschaft ein eingebettetes Objekt ist, wird die MOF-Darstellung des Objekts erstellt (ähnlich der Methode [**IWbemClassObject:: getobjecttext**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getobjecttext) ).
-   Wenn eine Eigenschaft eines eingebetteten Arrays von-Objekten angefordert wird, wird diese als Eigenschaft mit einem Array Wert behandelt. Beispiel:% MyEvents. TargetInstance. driverletter% kann "(" C: "," D: ")" ("C:", "D:") "(" C: "," D: ")" ergeben

## <a name="string-literals"></a>Zeichenfolgenliterale

Alles in einem Paar von Anführungszeichen wird als Zeichenfolgenliteralzeichen betrachtet und nicht ersetzt.

Das folgende Beispiel zeigt die Zeichenfolge, die der Compiler für "CPU-Auslastung ist% cpuausnutzung%" anzeigt.

``` syntax
CPU utilization is %CPUUtilization%
```

Diese Zeichenfolge erzeugt die folgende Ausgabe.

``` syntax
CPU utilization is 90
```

Andererseits wird die Zeichenfolge "CPU-Auslastung ( \\ % cpuausnutzung%") \\ wie folgt vom Compiler erkannt.

``` syntax
CPU utilization is "%CPUUtilization%"
```

Diese Zeichenfolge erzeugt die folgende Ausgabe ohne Variablen Ersetzung.

``` syntax
CPU utilization is "%CPUUtilization%"
```

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Überwachen von und reagieren auf Ereignisse mit Standard Consumern](monitoring-and-responding-to-events-with-standard-consumers.md)
</dt> </dl>

 

 



