---
title: UI-Richtlinien für NDF-Hilfsklassen Erweiterungen
description: Beim Erstellen einer Hilfsklasse müssen Sie Text erstellen, damit der Benutzer die Ursache eines Vorfalls und die möglichen Reparatur Schritte besser verstehen kann.
ms.assetid: f13f3621-ab82-4e22-9442-0a4d57c368fc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e48357ba6561ab135e2c341409c22d1edf3fb7d
ms.sourcegitcommit: 2e9db3c7d9a3dbea15196b03c883846fad6f32be
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/12/2019
ms.locfileid: "104313584"
---
# <a name="ui-guidelines-for-ndf-helper-class-extensions"></a>UI-Richtlinien für NDF-Hilfsklassen Erweiterungen

Beim Erstellen einer Hilfsklasse müssen Sie Text erstellen, damit der Benutzer die Ursache eines Vorfalls und die möglichen Reparatur Schritte besser verstehen kann.

## <a name="root-cause-and-repair"></a>Grundursache und Reparatur

Wenn ein Incident auftritt, wird ein Dialogfeld angezeigt, um den Benutzer darüber zu informieren, was passiert ist. Der von Ihnen erstellte Text wird in zwei separaten Bereichen angezeigt.

-   **Grundursache**: eine kurze Beschreibung der Ursache des Problems. Enthält Informationen, die einem Administrator oder einem erweiterten Benutzer helfen, das Problem zu beheben.
-   **Reparatur** Vorgang: erweitert die Grundursache, um weitere Details zu den Schritten zu erhalten, die ein Benutzer ausführen kann, ohne zu lange zu lange.

Jede Grundursache oder Reparatur sollte über einen Titel und eine Beschreibung verfügen. Der gesamte Text vor dem ersten " \\ n"-Zeichen wird für den Titel verwendet. Der gesamte Text, der auf das erste \\ Zeichen "n" folgt (einschließlich aller nachfolgenden Zeilenumbrüche), wird für die Beschreibung verwendet.

## <a name="title-guidelines"></a>Titel Richtlinien

Der Titel einer Grundursache oder Reparatur sollte den folgenden Richtlinien entsprechen:

-   Darf höchstens 128 Zeichen umfassen. (es werden 40 Zeichen oder weniger Zeichen empfohlen.)
-   Darf nicht mit einem-Zeitraum enden.

## <a name="description-guidelines"></a>Beschreibungen von Richtlinien

Die Beschreibung einer Grundursache oder Reparatur sollte den folgenden Richtlinien entsprechen:

-   Darf höchstens 512 Zeichen umfassen.
-   Jeder Satz sollte mit einem bestimmten Zeitraum enden.
-   Das \\ Zeichen "n" kann verwendet werden, um einen Zeilenumbruch in der Beschreibung zu erstellen.

 

 




