---
description: Die Umgebungs Zuordnung ist eine Technik, die hochgradig reflektierenden Oberflächen ohne Verwendung der Ray-Ablauf Verfolgung simuliert.
ms.assetid: vs|directx_sdk|~\environment_mapping.htm
title: Umgebungs Zuordnung (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 686f15b2f097550206f9c02cfc4104e7c9f6c030
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103745952"
---
# <a name="environment-mapping-direct3d-9"></a>Umgebungs Zuordnung (Direct3D 9)

Die Umgebungs Zuordnung ist eine Technik, die hochgradig reflektierenden Oberflächen ohne Verwendung der Ray-Ablauf Verfolgung simuliert. In der Praxis wendet die Umgebungs Zuordnung eine spezielle Textur Karte an, die ein Bild der Szene enthält, die ein Objekt für das Objekt selbst umgibt. Das Ergebnis ähnelt der Darstellung einer reflektierenden Oberfläche, so nah genug, um das Auge zu täuschen, ohne dass eine der komplexen Berechnungen an der Ray-Ablauf Verfolgung vorhanden ist.

In der folgenden Abbildung wird ein Typ der Umgebungs Zuordnung mit dem Namen sphärischen Umgebungs Zuordnung veranschaulicht. Weitere Informationen finden Sie unter [sphärischen Umgebungs Zuordnung](spherical-environment-mapping.md).

![Darstellung eines "Teekanne" mit einer angewendeten Textur, die die Umgebung reflektiert](images/spheremapped-teapot.png)

Die "Teekanne" in diesem Bild scheint der Umgebung widerzuspiegeln. Dabei handelt es sich tatsächlich um eine Textur, die auf das Objekt angewendet wird. Da die Umgebungs Zuordnung eine Textur in Kombination mit speziell berechneten Texturkoordinaten verwendet, kann Sie in Echtzeit ausgeführt werden.

Dieser Abschnitt enthält Informationen zum Durchführen von zwei gängigen Typen der Umgebungs Zuordnung mit Direct3D. Es gibt viele Arten von Umgebungs Zuordnung, die in der gesamten Grafikbranche verwendet werden. die folgenden Themen Zielen jedoch auf die beiden gängigsten Formen ab: kubische Umgebungs Zuordnung und sphärischen Umgebungs Zuordnung.

-   [Kubische Umgebungs Zuordnung](cubic-environment-mapping.md)
-   [Sphärischen Umgebungs Zuordnung](spherical-environment-mapping.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Pixel Pipeline](pixel-pipeline.md)
</dt> </dl>

 

 



