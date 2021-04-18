---
description: Nachdem Sie den Suchergebnis Modus, den Durchsuchenmodus und die Layoutmuster verstanden haben, können Sie eine benutzerdefinierte Eigenschaften Liste für den Dateityp registrieren. Führen Sie diese Schritte aus, um eine benutzerdefinierte Eigenschaften Liste und ein Layoutmuster für den Dateityp zu registrieren.
ms.assetid: 29B863B3-E5FD-4E0A-B76B-4AFE5A6A76E3
title: Registrieren von benutzerdefinierten Eigenschaften und Layouts für den Dateityp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da55d0a90d4dd0f3ca109a3ca9f628a3c0912520
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104994662"
---
# <a name="how-to-register-custom-properties-and-layout-for-your-file-type"></a>Registrieren von benutzerdefinierten Eigenschaften und Layouts für den Dateityp

Nachdem Sie den Suchergebnis Modus, den Durchsuchenmodus und die Layoutmuster verstanden haben, können Sie eine benutzerdefinierte Eigenschaften Liste für den Dateityp registrieren.

Führen Sie diese Schritte aus, um eine benutzerdefinierte Eigenschaften Liste und ein Layoutmuster für den Dateityp zu registrieren.

## <a name="instructions"></a>Instructions

### <a name="step-1"></a>Schritt 1:

Wählen Sie aus den vier layoutmustern: Alpha, Beta, Gamma oder Delta.

### <a name="step-2"></a>Schritt 2:

Berücksichtigen Sie die folgenden Formatierungs Regeln, die gleichermaßen für alle vier Layoutmuster gelten:

-   Eigenschaft 1 wird immer in einer größeren Schriftgröße angezeigt. Der Umfang der großen Schriftart, der in der Regel für den Elementnamen verwendet wird, aber auch für den Anker oder eine andere Element Eigenschaft verwendet werden kann.
-   Eigenschaft 4 ist für Ausschnitte in den Alpha-, Beta-und Gamma layoutmustern vorgesehen. Dieser Eigenschaft wird mehr Platz in diesen Mustern zugewiesen, und Sie wird in einer grauen Schriftfarbe angezeigt, im Gegensatz zu den anderen Eigenschaften, um Sie zu unterstützen.
-   Die unten angegebenen Pixel Messungen liegen in relativen Pixeln vor, und die Größe enthält das Symbol/die Miniaturansicht links neben den Eigenschaften und das Leerzeichen zwischen Symbol/Miniaturansicht und Auswahl Rechteck.
-   Die meisten Eigenschaften verfügen über eine minimale Anzeige Größe. Aus diesem Grund werden Sie nicht angezeigt, wenn auf einer bestimmten Ansichts Größe nicht genügend Speicherplatz vorhanden ist. Die minimale Größe ist normalerweise 100 Pixel breit.
-   Jedes Layoutmuster definiert die Anzahl der Zeilen und die Anzahl der Eigenschaften in jeder Zeile.

### <a name="step-3"></a>Schritt 3:

Entscheiden Sie, welche Eigenschaften im Layout angezeigt werden sollen und welche Eigenschaft Sie an jedem Speicherort anzeigen möchten. Berücksichtigen Sie bei der Entscheidung, welche Eigenschaft an jeder Position im Layout angezeigt werden soll, die typische Länge der Eigenschaft, ihre Wichtigkeit für den Benutzer und ob Sie gelöscht werden soll, wenn die Fenstergröße zu klein ist, um alle Eigenschaften zu enthalten.

### <a name="step-4"></a>Schritt 4:

Registrieren Sie ein Layoutmuster und eine Eigenschaften Liste für Ihren Dateityp oder Elementtyp, indem Sie die folgenden Schlüssel unter dem ProgID-Registrierungsschlüssel für den Dateityp oder das Element hinzufügen (in diesem Beispiel für den Dateityp ". xyz").

```
HKEY_CLASSES_ROOT\*
   Contoso.xyzfile
      (ContentViewModeForBrowse) = <Layout pattern name (Alpha, Beta, Delta, or Gamma)>
      (ContentViewModeForSearch) = <Layout pattern name (Alpha, Beta, Delta, or Gamma)>
      (ContentViewModeLayoutPatternForBrowse) = <PropertyList>
      (ContentViewModeLayoutPatternForSearch) = <PropertyList>
```

### <a name="step-5"></a>Schritt 5:

Beachten Sie die folgenden Formatierungs Richtlinien zum Registrieren von Eigenschaften:

-   Jede Registrierung beginnt mit `prop:`
-   Jede Eigenschaft erfordert den vollständigen Eigenschaftsnamen.
-   Eigenschaften werden durch ein Semikolon ohne Leerzeichen voneinander getrennt.
-   Eigenschaften werden in der Reihenfolge angezeigt, in der das ausgewählte Layoutmuster definiert ist.
-   `~` Gibt an, dass die Eigenschaften Bezeichnung nicht angezeigt werden soll.
-   `~System.LayoutPattern.PlaceHolder` sollte verwendet werden, wenn Sie eine im Layoutmuster angegebene Eigenschaft leer lassen möchten.

Der folgende Beispiel Registrierungsschlüssel veranschaulicht diese Formatierungs Richtlinien.

```
HKEY_CLASSES_ROOT\
   Kind.Document
      (ContentViewModeForBrowse) = <PropertyList>
```

Mögliche Werte für (contentviewmodeforbrowse) umfassen Folgendes: `prop:~System.ItemNameDisplay;System.Author;System.LayoutPattern.Placeholder;System.Keywords;System.DateModified;~System.Size`

 

 



