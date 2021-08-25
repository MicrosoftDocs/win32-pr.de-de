---
description: Im Folgenden finden Sie einige allgemeine Instanzen von bedingten Anweisungen. Weitere Informationen finden Sie unter Syntax der bedingten Anweisung.
ms.assetid: 8b6bae7a-20ae-494c-bd96-66bd537c8630
title: Beispiele für die Syntax der bedingten Anweisung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88445e1e4b371669c43b47d1ca54e9fd677c5414985ade3908b95e00717de887
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119811030"
---
# <a name="examples-of-conditional-statement-syntax"></a>Beispiele für die Syntax der bedingten Anweisung

Im Folgenden finden Sie einige allgemeine Instanzen von bedingten Anweisungen. Weitere Informationen finden Sie unter Syntax der [bedingten Anweisung.](conditional-statement-syntax.md)

## <a name="run-action-on-removal"></a>Führen Sie die Aktion beim Entfernen aus.

Weitere Informationen finden Sie unter [Durchführen von Aktionen, die während des Entfernens ausgeführt werden sollen.](conditioning-actions-to-run-during-removal.md)

## <a name="run-action-only-if-the-product-has-not-been-installed"></a>Führen Sie die Aktion nur aus, wenn das Produkt nicht installiert wurde.

``` syntax
NOT Installed
```

## <a name="run-action-only-if-the-product-will-be-installed-local-do-not-run-action-on-a-reinstallation"></a>Führen Sie die Aktion nur aus, wenn das Produkt lokal installiert wird. Führen Sie keine Aktion für eine Neuinstallation aus.

``` syntax
(&FeatureName=3) AND NOT(!FeatureName=3)
```

Der Begriff "&FeatureName=3" bedeutet, dass die Aktion darin besteht, das Feature lokal zu installieren. Der Begriff "NOT(! FeatureName=3)" bedeutet, dass das Feature nicht lokal installiert ist.

## <a name="run-action-only-if-the-feature-will-be-uninstalled"></a>Führen Sie die Aktion nur aus, wenn das Feature deinstalliert wird.

``` syntax
(&FeatureName=2) AND (!FeatureName=3)
```

Diese Bedingung überprüft nur den Übergang des Features von einem installierten Zustand von "local" in den "absent"-Zustand.

## <a name="run-action-only-if-the-component-was-installed-local-but-is-transitioning-out-of-state"></a>Führen Sie die Aktion nur aus, wenn die Komponente lokal installiert wurde, aber den Zustand übergeht.

``` syntax
(?ComponentName=3) AND ($ComponentName=2 OR $ComponentName=4)
```

Der Begriff "? ComponetName=3" bedeutet, dass die Komponente lokal installiert ist. Der Begriff "$ComponentName=2" bedeutet, dass der Aktionszustand für die Komponente Absent lautet. Der Begriff "$ComponentName=4" bedeutet, dass der Aktionszustand der Komponente von der Quelle aus ausgeführt wird. Beachten Sie, dass der Aktionsstatus ankündigen für eine Komponente ungültig ist.

## <a name="run-action-only-on-the-reinstallation-of-a-component"></a>Führen Sie die Aktion nur für die Neuinstallation einer Komponente aus.

``` syntax
?ComponentName=$ComponentName
```

## <a name="run-action-only-when-a-particular-patch-is-applied"></a>Führen Sie die Aktion nur aus, wenn ein bestimmter Patch angewendet wird.

``` syntax
PATCH AND PATCH >< MEDIASRCPROPNAME
```

Weitere Informationen finden Sie im Abschnitt "Hinweise" auf der [**PATCH-Eigenschaftenseite.**](patch.md)

 

 



