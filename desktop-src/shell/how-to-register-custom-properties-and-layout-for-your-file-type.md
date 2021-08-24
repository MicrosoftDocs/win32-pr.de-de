---
description: Nachdem Sie den Suchergebnismodus, den Durchsuchen-Modus und die Layoutmuster verstanden haben, können Sie eine benutzerdefinierte Eigenschaftenliste für Ihren Dateityp registrieren. Führen Sie die folgenden Schritte aus, um eine benutzerdefinierte Eigenschaftenliste und ein Layoutmuster für Ihren Dateityp zu registrieren.
ms.assetid: 29B863B3-E5FD-4E0A-B76B-4AFE5A6A76E3
title: Registrieren von benutzerdefinierten Eigenschaften und Layouts für Ihren Dateityp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9388965a781d4104ae13de689b72208a8b69e213a758c9b34552c03bb938453
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119714900"
---
# <a name="how-to-register-custom-properties-and-layout-for-your-file-type"></a>Registrieren von benutzerdefinierten Eigenschaften und Layouts für Ihren Dateityp

Nachdem Sie den Suchergebnismodus, den Durchsuchen-Modus und die Layoutmuster verstanden haben, können Sie eine benutzerdefinierte Eigenschaftenliste für Ihren Dateityp registrieren.

Führen Sie die folgenden Schritte aus, um eine benutzerdefinierte Eigenschaftenliste und ein Layoutmuster für Ihren Dateityp zu registrieren.

## <a name="instructions"></a>Anweisungen

### <a name="step-1"></a>Schritt 1:

Wählen Sie aus den vier Layoutmustern Alpha, Beta, Gamma oder Delta aus.

### <a name="step-2"></a>Schritt 2:

Beachten Sie die folgenden Formatierungsregeln, die gleichermaßen für alle vier Layoutmuster gelten:

-   Eigenschaft 1 wird immer in einem größeren Schriftgrad angezeigt. Der große Schriftgrad, der normalerweise für den Elementnamen verwendet wird, kann aber auch für den Anker oder eine andere Elementeigenschaft verwendet werden.
-   Eigenschaft 4 ist für Ausschnitte in den Layoutmustern Alpha, Beta und Gamma vorgesehen. Diese Eigenschaft wird mehr Platz in diesen Mustern zugewiesen und wird in grauer Schriftfarbe angezeigt, im Gegensatz zu Schwarz wie die anderen Eigenschaften, um sie zu unterstützen.
-   Die folgenden Pixelmessungen sind in relativen Pixeln angegeben, und die Größe umfasst das Symbol/die Miniaturansicht links neben den Eigenschaften und den Abstand zwischen dem Symbol/der Miniaturansicht und dem Auswahlrechteck.
-   Die meisten Eigenschaften haben eine mindeste Anzeigegröße. Daher werden sie nicht angezeigt, wenn nicht genügend Platz für sie in einer bestimmten Ansichtsgröße vorhanden ist. Die Mindestgröße ist in der Regel 100 Pixel breit.
-   Jedes Layoutmuster definiert die Anzahl der Zeilen und die Anzahl der Eigenschaften in jeder Zeile.

### <a name="step-3"></a>Schritt 3:

Entscheiden Sie, welche Eigenschaften sie im Layout anzeigen möchten und welche Eigenschaft Sie an den einzelnen Speicherorten anzeigen möchten. Berücksichtigen Sie bei der Entscheidung, welche Eigenschaft an jeder Position im Layout angezeigt werden soll, die typische Länge der Eigenschaft, ihre Wichtigkeit für den Benutzer und ob sie gelöscht werden soll, wenn die Fenstergröße zu klein ist, um alle Eigenschaften zu enthalten.

### <a name="step-4"></a>Schritt 4:

Registrieren Sie ein Layoutmuster und eine Eigenschaftenliste für Ihren Dateityp oder Elementtyp, indem Sie die folgenden Schlüssel unter dem ProgID-Registrierungsschlüssel für den Dateityp oder das Element hinzufügen (in diesem Beispiel für den Dateityp .xyz).

```
HKEY_CLASSES_ROOT\*
   Contoso.xyzfile
      (ContentViewModeForBrowse) = <Layout pattern name (Alpha, Beta, Delta, or Gamma)>
      (ContentViewModeForSearch) = <Layout pattern name (Alpha, Beta, Delta, or Gamma)>
      (ContentViewModeLayoutPatternForBrowse) = <PropertyList>
      (ContentViewModeLayoutPatternForSearch) = <PropertyList>
```

### <a name="step-5"></a>Schritt 5:

Beachten Sie die folgenden Formatierungsrichtlinien zum Registrieren von Eigenschaften:

-   Jede Registrierung beginnt mit `prop:`
-   Jede Eigenschaft erfordert den vollständigen Eigenschaftennamen.
-   Eigenschaften werden durch ein Semikolon ohne Leerzeichen getrennt.
-   Eigenschaften werden in der Reihenfolge angezeigt, die durch das ausgewählte Layoutmuster definiert ist.
-   `~` gibt an, dass die Eigenschaftenbezeichnung nicht angezeigt werden soll.
-   `~System.LayoutPattern.PlaceHolder` sollte verwendet werden, wenn Sie eine Eigenschaft leer lassen möchten, die im Layoutmuster angegeben ist.

Der folgende Beispielregistrierungsschlüssel veranschaulicht diese Formatierungsrichtlinien.

```
HKEY_CLASSES_ROOT\
   Kind.Document
      (ContentViewModeForBrowse) = <PropertyList>
```

Mögliche Werte für (ContentViewModeForBrowse) sind: `prop:~System.ItemNameDisplay;System.Author;System.LayoutPattern.Placeholder;System.Keywords;System.DateModified;~System.Size`

 

 



