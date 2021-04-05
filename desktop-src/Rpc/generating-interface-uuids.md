---
title: Erstellen von Schnittstellen-UUIDs
description: Erstellen von Universal Unique Identifier (UUIDs) der Schnittstelle und Verwenden von uuidgen.
ms.assetid: a973b7f9-71c5-46a0-aa0c-51f150560dbc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68c5f727ed3e37139d4da50f84c3929bff333156
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103710205"
---
# <a name="generating-interface-uuids"></a>Erstellen von Schnittstellen-UUIDs

Dieser Abschnitt enthält Informationen zu universellen eindeutigen Bezeichnerzeichen (UUIDs) und zum uuidgen-Hilfsprogramm in den folgenden Themen:

-   [Was ist eine UUID?](#what-is-a-uuid)
-   [Verwenden von uuidgen](#using-uuidgen)

## <a name="what-is-a-uuid"></a>Was ist eine UUID?

Alle Schnittstellen müssen in einem Netzwerk eindeutig identifiziert werden, damit Sie von Clients gefunden werden können. In kleinen Netzwerken kann der Name der Schnittstelle allein ausreichen, um Sie zu identifizieren. Dies ist jedoch in großen Netzwerken in der Regel nicht möglich. Daher weisen Entwickler in der Regel jeder Schnittstelle einen universellen eindeutigen Bezeichner (UUID, austauschbar mit dem Begriff GUID oder einen global eindeutigen Bezeichner) zu. Eine UUID ist eine Zeichenfolge, die eine Reihe von hexadezimalen Ziffern enthält. Jede Schnittstelle hat eine andere UUID. Weitere Informationen finden Sie unter [Zeichenfolge UUID](string-uuid.md).

Die Textdarstellung einer UUID ist eine Zeichenfolge, die aus 8 hexadezimalen Ziffern gefolgt von einem Bindestrich gefolgt von drei durch Trennzeichen getrennten Gruppen von vier hexadezimalen Ziffern gefolgt von einem Bindestrich gefolgt von 12 hexadezimal Ziffern besteht. Das folgende Beispiel ist eine gültige UUID-Zeichenfolge:

ba209999-0c6c-11d2-97cf-00c04f8eea45

Leere UUIDs werden als NULL UUIDs anstelle von **null** UUIDs bezeichnet. Der Begriff Nil gibt alles an, das NULL, leer, leer oder nicht initialisiert ist. Eine leere Zeichenfolge, ein leerer Datenbankdaten Satz oder eine nicht initialisierte UUID sind Beispiele für Nil-Werte.

> [!Note]  
> Der Wert **null** ist der spezifische Wert 0 (null). Sie wird häufig in der C-und C++-Programmierung zusammen mit Zeigern verwendet. Nil ist ein allgemeinerer Begriff als **null**. Nicht initialisierte UUIDs der Objektschnittstelle sollten immer als NULL-UUIDs und nicht als **null** -UUIDs bezeichnet werden.

 

## <a name="using-uuidgen"></a>Verwenden von uuidgen

Microsoft stellt ein hilfsprogrammprogramm mit dem Namen uuidgen zum Generieren der UUIDs zur Verfügung. Das Hilfsprogramm uuidgen generiert die UUID im IDL-Dateiformat oder im C-sprach Format.

Wenn Sie das Hilfsprogramm uuidgen von der Befehlszeile ausführen, können Sie die folgenden Befehls Schalter verwenden.



| Uuidgen-Switch           | BESCHREIBUNG                                                                |
|--------------------------|----------------------------------------------------------------------------|
| **/I**                   | Gibt UUID an eine IDL-Schnittstellen Vorlage aus.                                 |
| **/s**                   | Gibt UUID als initialisierte C-Struktur aus.                                |
| **/o** < *Dateiname*> | Leitet die Ausgabe in eine Datei um. wird unmittelbar nach dem **/o** -Schalter angegeben. |
| **/n** < *Zahl*>   | Gibt die Anzahl der zu generierenden UUIDs an.                                 |
| **/v**                   | Zeigt Versionsinformationen zu uuidgen an.                                |
| **/h** oder **?**          | Zeigt die Zusammenfassung der Befehls Option an.                                           |



 

In der Regel verwenden Sie das Hilfsprogramm uuidgen, wie im folgenden Beispiel gezeigt.

**"uuidgen-i-omyapp. idl**

Dieser Befehl generiert eine UUID und speichert Sie in einer Mittel l-Datei, die Sie als Vorlage verwenden können. Wenn der vorherige Befehl ausgeführt wird, ähnelt der Inhalt von "MyApp. idl" folgendem:

``` syntax
[
  uuid(ba209999-0c6c-11d2-97cf-00c04f8eea45),
  version(1.0)
]
interface INTERFACENAME
{

}
```

Der nächste Schritt besteht darin, den Platzhalter Namen "interfakename" durch den tatsächlichen Namen der Schnittstelle zu ersetzen.

 

 




