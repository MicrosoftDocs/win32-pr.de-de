---
description: Im folgenden finden Sie einige allgemeine Instanzen von Bedingungs Anweisungen. Weitere Informationen finden Sie unter bedingte Anweisungs Syntax.
ms.assetid: 8b6bae7a-20ae-494c-bd96-66bd537c8630
title: Beispiele für bedingte Anweisungs Syntax
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca91a2b3e89160fad19ad5d9b1c6a3d33929e5d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959438"
---
# <a name="examples-of-conditional-statement-syntax"></a>Beispiele für bedingte Anweisungs Syntax

Im folgenden finden Sie einige allgemeine Instanzen von Bedingungs Anweisungen. Weitere Informationen finden Sie unter [bedingte Anweisungs Syntax](conditional-statement-syntax.md).

## <a name="run-action-on-removal"></a>Aktion beim Entfernen ausführen.

Weitere Informationen finden Sie unter durch [führen von während des Entfernens](conditioning-actions-to-run-during-removal.md)auszuführenden Aktivitäten.

## <a name="run-action-only-if-the-product-has-not-been-installed"></a>Führen Sie die Aktion nur aus, wenn das Produkt nicht installiert wurde.

``` syntax
NOT Installed
```

## <a name="run-action-only-if-the-product-will-be-installed-local-do-not-run-action-on-a-reinstallation"></a>Führen Sie die Aktion nur aus, wenn das Produkt lokal installiert wird. Führen Sie die Aktion bei einer erneuten Installation nicht aus.

``` syntax
(&FeatureName=3) AND NOT(!FeatureName=3)
```

Der Begriff "&Featurename = 3" bedeutet, dass die Funktion lokal installiert werden muss. Der Begriff "Not (! Featurename = 3) "bedeutet, dass das Feature nicht lokal installiert ist.

## <a name="run-action-only-if-the-feature-will-be-uninstalled"></a>Aktion nur ausführen, wenn die Funktion deinstalliert wird.

``` syntax
(&FeatureName=2) AND (!FeatureName=3)
```

Diese Bedingung überprüft nur, ob die Funktion vom installierten Zustand "lokal" in den Zustand "nicht vorhanden" übergeht.

## <a name="run-action-only-if-the-component-was-installed-local-but-is-transitioning-out-of-state"></a>Die Aktion wird nur ausgeführt, wenn die Komponente lokal installiert wurde, sich jedoch außerhalb des Zustands befindet.

``` syntax
(?ComponentName=3) AND ($ComponentName=2 OR $ComponentName=4)
```

Der Begriff "? Componetname = 3 "bedeutet, dass die Komponente lokal installiert ist. Der Begriff "$ComponentName = 2" bedeutet, dass der Aktionszustand für die Komponente nicht vorhanden ist. Der Begriff "$ComponentName = 4" bedeutet, dass der Aktionszustand für die Komponente aus der Quelle ausgeführt wird. Beachten Sie, dass der Aktions Status ankündigen für eine Komponente nicht gültig ist.

## <a name="run-action-only-on-the-reinstallation-of-a-component"></a>Aktion nur für die Neuinstallation einer Komponente ausführen.

``` syntax
?ComponentName=$ComponentName
```

## <a name="run-action-only-when-a-particular-patch-is-applied"></a>Aktion nur ausführen, wenn ein bestimmter Patch angewendet wird.

``` syntax
PATCH AND PATCH >< MEDIASRCPROPNAME
```

Weitere Informationen finden Sie im Abschnitt "Hinweise" auf der Eigenschaften Seite " [**Patch**](patch.md) ".

 

 



