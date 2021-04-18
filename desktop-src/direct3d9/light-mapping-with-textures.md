---
description: Damit eine Anwendung eine 3D-Szene realistisch darstellen kann, muss Sie die Auswirkungen berücksichtigen, die Lichtquellen auf die Darstellung der Szene haben.
ms.assetid: ff2037e4-2cf6-4247-b93f-13f0078f3b58
title: Einfache Zuordnung mit Texturen (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5652446562e4c66390d67e11fa624a4a5659b85
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106338870"
---
# <a name="light-mapping-with-textures-direct3d-9"></a>Einfache Zuordnung mit Texturen (Direct3D 9)

Damit eine Anwendung eine 3D-Szene realistisch darstellen kann, muss Sie die Auswirkungen berücksichtigen, die Lichtquellen auf die Darstellung der Szene haben. Obwohl Techniken wie flache und Gouraud-Schattierung in dieser Hinsicht wertvolle Tools sind, können Sie für Ihre Bedürfnisse nicht ausreichen. Direct3D unterstützt Multipass-und mehrere Textur Mischungen. Diese Funktionen ermöglichen es der Anwendung, Szenen durch eine realistischere Darstellung zu rendern als Szenen, die ausschließlich mit Schattierungs Techniken gerendert werden. Indem Sie eine oder mehrere Beleuchtungs Zuordnungen anwenden, kann die Anwendung Bereiche von Licht und Schatten den primitiven zuordnen.

Eine helle Karte ist eine Textur oder eine Gruppe von Texturen, die Informationen zur Beleuchtung in einer 3D-Szene enthält. Sie können die Beleuchtungs Informationen in den Alpha Werten der hellen Karte, in den Farbwerten oder in beiden speichern.

Wenn Sie eine einfache Zuordnung mithilfe der Multipass-Textur Mischung implementieren, sollte Ihre Anwendung die lichtkarte auf die primitiven beim ersten Durchlauf rendern. Zum Rendern der Basis Textur sollte ein zweiter Durchlauf verwendet werden. Die Ausnahme bildet die Glanzlicht Zuordnung. In diesem Fall müssen Sie zuerst die Basis Textur erzeugen; Fügen Sie dann die helle Karte hinzu.

Mehrere Textur Mischungs Eigenschaften ermöglichen der Anwendung das Rendern der hellen Karte und der Basis Textur in einem Durchlauf. Wenn die Hardware des Benutzers mehrere Textur Mischungs Maßnahmen bereitstellt, sollte Sie von der Anwendung beim Durchführen einer hellen Zuordnung genutzt werden. Dies verbessert die Leistung Ihrer Anwendung erheblich.

Mithilfe von hellen Karten kann eine Direct3D-Anwendung eine Vielzahl von Beleuchtungs Effekten erzielen, wenn Sie primitive rendert. Sie kann nicht nur monochrome und farbige Beleuchtung in einer Szene zuordnen, sondern auch Details wie Glanzlichter und diffuse Beleuchtung hinzufügen.

Informationen zur Verwendung der Direct3D-Textur Mischung zum Durchführen einer einfachen Zuordnung finden Sie in den folgenden Themen.

-   [Monochrome helle Karten (Direct3D 9)](monochrome-light-maps.md)
-   [Farb hellen Karten (Direct3D 9)](color-light-maps.md)
-   [Glanzlichter Karten (Direct3D 9)](specular-light-maps.md)
-   [Diffuses Licht Maps (Direct3D 9)](diffuse-light-maps.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Textur Mischung](texture-blending.md)
</dt> </dl>

 

 



