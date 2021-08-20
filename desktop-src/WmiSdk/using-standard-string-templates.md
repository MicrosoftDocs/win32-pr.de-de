---
description: Mehrere Consumer, z. B. der Active Script-Ereignis-Consumer oder der Befehlszeilenereignis-Consumer, verfügen über Zeichenfolgeneigenschaften mit dem Vorlagenqualifizierer.
ms.assetid: d734c226-e160-4834-a5e8-62390905dfde
ms.tgt_platform: multiple
title: Verwenden von Standardzeichenfolgenvorlagen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c60a28730b890a5e922489a47b5b382b545cd6712d61cb976e96b549039ef7d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119049938"
---
# <a name="using-standard-string-templates"></a>Verwenden von Standardzeichenfolgenvorlagen

Mehrere Consumer, z. B. der Active Script-Ereignis-Consumer oder  der Befehlszeilenereignis-Consumer, verfügen über Zeichenfolgeneigenschaften mit dem Vorlagenqualifizierer. Diese Eigenschaften verwenden Standardzeichenfolgenvorlagen, um eine Zeichenfolge zu erstellen, die teilweise von der Consumerinstanz und teilweise von einem Ereignis konfiguriert wird. Die Struktur einer Standardzeichenfolgenvorlage ähnelt der Spezifikation der Umgebungsvariablen microsoft Windows.

Die folgende Liste enthält einige Beispiele für die Vorlagensprache:

-   Die Zeichenfolge "Some text here" erzeugt immer die Zeichenfolge "Some text here".
-   "%CPUUtilization%" erzeugt immer den Wert der **CPUUtilization-Eigenschaft** des ereignisses, das übermittelt wird. Wenn die Eigenschaft keine Zeichenfolge ist, wird sie in eine Zeichenfolge konvertiert. Beispiel: "90" oder "TRUE".
-   "Die CPU-Auslastung dieses Prozessors ist zu diesem Zeitpunkt %CPUUtilization%", bettet den Wert der **CPUUtilization-Eigenschaft** des Ereignisses in die Zeichenfolge ein und erzeugt etwa "Die CPU-Auslastung dieses Prozessors beträgt zu diesem Zeitpunkt 90".
-   "%TargetInstance.CPUUtilization%" ruft den Wert der **CPUUtilization-Eigenschaft** in der eingebetteten Instanz der **TargetInstance-Eigenschaft** ab.
-   "%%" erzeugt ein einzelnes % -Zeichen.
-   Wenn die abgerufene Eigenschaft ein Array ist, wird das gesamte Array im folgenden Format erstellt: "(1,5,10,1024)". Wenn nur ein Element im Array vorhanden ist, werden die Klammern ausgelassen. Wenn im Array keine Elemente vorhanden sind, wird "()" erstellt.
-   Wenn eine Eigenschaft ein eingebettetes Objekt ist, wird die MOF-Darstellung des Objekts erstellt (ähnlich der [**IWbemClassObject::GetObjectText-Methode).**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getobjecttext)
-   Wenn eine Eigenschaft eines eingebetteten Arrays von -Objekten angefordert wird, wird sie als Eigenschaft mit einem Arraywert behandelt. Beispiel: %MyEvents.TargetInstance.DriverLetter% könnte "("C:","D:")" erzeugen, wenn MyEvents ein Array eingebetteter Instanzänderungsereignisse ist.

## <a name="string-literals"></a>Zeichenfolgenliterale

Alles innerhalb eines Paars von Anführungszeichen gilt als Zeichenfolgenliteral und wird nicht ersetzt.

Das folgende Beispiel zeigt die Zeichenfolge, die der Compiler für "CPU-Auslastung ist %CPUUtilization%" erkennt.

``` syntax
CPU utilization is %CPUUtilization%
```

Diese Zeichenfolge erzeugt die folgende Ausgabe.

``` syntax
CPU utilization is 90
```

Auf der anderen Seite wird die Zeichenfolge "CPU-Auslastung ist \\ "%CPUUtilization% \\ "" vom Compiler wie folgt angezeigt.

``` syntax
CPU utilization is "%CPUUtilization%"
```

Diese Zeichenfolge erzeugt die folgende Ausgabe ohne Variablenersetzung.

``` syntax
CPU utilization is "%CPUUtilization%"
```

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Überwachen und Reagieren auf Ereignisse mit Standard-Consumern](monitoring-and-responding-to-events-with-standard-consumers.md)
</dt> </dl>

 

 



