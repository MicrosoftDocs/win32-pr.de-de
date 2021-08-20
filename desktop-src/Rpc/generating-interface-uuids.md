---
title: Generieren von Schnittstellen-UUIDs
description: Generieren von UUIDs (Universal Unique Identifiers) der Schnittstelle und Verwenden von Uuidgen.
ms.assetid: a973b7f9-71c5-46a0-aa0c-51f150560dbc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70c21ead6161a79d000d2741a49c4fb61ff23b3a8a3340db2eb26a7805424df5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118929547"
---
# <a name="generating-interface-uuids"></a>Generieren von Schnittstellen-UUIDs

Dieser Abschnitt enthält Informationen zu UUIDs (Universal Unique Identifiers) und dem Uuidgen-Hilfsprogramm in den folgenden Themen:

-   [Was ist eine UUID?](#what-is-a-uuid)
-   [Verwenden von Uuidgen](#using-uuidgen)

## <a name="what-is-a-uuid"></a>Was ist eine UUID?

Alle Schnittstellen müssen in einem Netzwerk eindeutig identifiziert werden, damit Clients sie finden können. In kleinen Netzwerken kann der Name der Schnittstelle allein ausreichen, um sie zu identifizieren. Dies ist jedoch in großen Netzwerken in der Regel nicht möglich. Daher weisen Entwickler jeder Schnittstelle in der Regel einen UUID (Universal Unique Identifier) zu, der mit dem Begriff GUID oder Globally Unique Identifier austauschbar ist. Eine UUID ist eine Zeichenfolge, die einen Satz von Hexadezimalziffern enthält. Jede Schnittstelle verfügt über eine andere UUID. Weitere Informationen finden Sie unter [String UUID](string-uuid.md).

Die Textdarstellung einer UUID ist eine Zeichenfolge, die aus acht Hexadezimalziffern gefolgt von einem Bindestrich gefolgt von drei durch Bindestriche getrennten Gruppen mit vier Hexadezimalziffern gefolgt von einem Bindestrich gefolgt von 12 Hexadezimalziffern besteht. Das folgende Beispiel ist eine gültige UUID-Zeichenfolge:

ba209999-0c6c-11d2-97cf-00c04f8eea45

Leere UUIDs werden anstelle von NULL-UUIDs als NULL-UUIDs bezeichnet.  Der Begriff nil gibt alles an, was null, leer, leer oder nicht initialisiert ist. Eine leere Zeichenfolge, ein leerer Datenbankdatensatz oder eine nicht initialisierte UUID sind Beispiele für NULL-Werte.

> [!Note]  
> Der Wert **NULL ist** der spezifische Wert 0 (null). Er wird häufig in C- und C++-Programmierung in Verbindung mit Zeigern verwendet. Nil ist ein allgemeinerer Begriff als **NULL.** Nicht initialisierte Objektschnittstellen-UUIDs sollten immer als NULL-UUIDs und nicht als NULL-UUIDs bezeichnet werden. 

 

## <a name="using-uuidgen"></a>Verwenden von Uuidgen

Microsoft stellt ein Hilfsprogramm namens Uuidgen zur Verfügung, um Ihre UUIDs zu generieren. Das Uuidgen-Hilfsprogramm generiert die UUID im IDL-Dateiformat oder C-Sprachformat.

Wenn Sie das Uuidgen-Hilfsprogramm über die Befehlszeile ausführen, können Sie die folgenden Befehlsschalter verwenden.



| Uuidgen-Schalter           | BESCHREIBUNG                                                                |
|--------------------------|----------------------------------------------------------------------------|
| **/I**                   | Gibt UUID in eine IDL-Schnittstellenvorlage aus.                                 |
| **/s**                   | Gibt UUID als initialisierte C-Struktur aus.                                |
| **/o** < *Dateiname*> | Leitet die Ausgabe an eine Datei um. wird unmittelbar nach dem **Schalter /o** angegeben. |
| **/n** < *number*>   | Gibt die Anzahl der zu generierenden UUIDs an.                                 |
| **/v**                   | Zeigt Versionsinformationen zu Uuidgen an.                                |
| **/h** oder **?**          | Zeigt eine Zusammenfassung der Befehlsoption an.                                           |



 

In der Regel verwenden Sie das Hilfsprogramm Uuidgen, wie im folgenden Beispiel gezeigt.

**uuidgen -i -oMyApp.idl**

Dieser Befehl generiert eine UUID und speichert sie in einer MIDL-Datei, die Sie als Vorlage verwenden können. Wenn der vorherige Befehl ausgeführt wird, sieht der Inhalt von MyApp.idl etwa wie folgt aus:

``` syntax
[
  uuid(ba209999-0c6c-11d2-97cf-00c04f8eea45),
  version(1.0)
]
interface INTERFACENAME
{

}
```

Der nächste Schritt besteht im Ersetzen des Platzhalternamens INTERFACENAME durch den tatsächlichen Namen Ihrer Schnittstelle.

 

 




