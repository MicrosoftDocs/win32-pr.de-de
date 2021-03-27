---
title: Dynamisches Verknüpfen
description: Grafik Entwickler erstellen manchmal große, allgemeine Shader, die von einer Vielzahl von Szenen Elementen verwendet werden können.
ms.assetid: 2f5f7852-0f0a-4fad-a412-9a0d634c73b6
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d5cd10bab8e2b4a28458cad1050847e0184ce43b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103710860"
---
# <a name="dynamic-linking"></a>Dynamisches Verknüpfen

Grafik Entwickler erstellen manchmal große, allgemeine Shader, die von einer Vielzahl von Szenen Elementen verwendet werden können. Zur Laufzeit führt der Shader bedingt Code aus, der für die jeweilige Situation geeignet ist. Leider verwenden diese großen, allgemeinen Shader allgemeine Register (GPRS) ineffizient und können viel langsamer als kleinere, gezieltere Shader sein.

Shader Model 5 löst dieses Leistungsproblem durch die Einführung dynamischer shaderverknüpfungen. Dynamisches Verknüpfen trennt Shader-Code Fragmente mithilfe von Schnittstellen und virtuellen Funktionen und ermöglicht es der Anwendung, das zu verwendende Fragment zur zeichnungszeit auszuwählen. Dies verbessert die Leistung, indem nur der benötigte Shader-Code und nicht der gesamte große Shader für allgemeine Zwecke gebunden wird.

## <a name="in-this-section"></a>In diesem Abschnitt



| Element                                                                                                                                                                                                                                                                                                                         | BESCHREIBUNG                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span id="Storing_Variables_and_Types_for_Shaders_to_Share"></span><span id="storing_variables_and_types_for_shaders_to_share"></span><span id="STORING_VARIABLES_AND_TYPES_FOR_SHADERS_TO_SHARE"></span>[Speichern von Variablen und Typen für die Freigabe von Shadern](storing-variables-and-types-for-shaders-to-share.md)<br/> | Beschreibt das Klassen Verknüpfungs Objekt zum Speichern von Variablen und Typen, die von mehreren Shadern gemeinsam genutzt werden können.<br/> |
| <span id="Interfaces_and_Classes"></span><span id="interfaces_and_classes"></span><span id="INTERFACES_AND_CLASSES"></span>[Schnittstellen und Klassen](overviews-direct3d-11-hlsl-dynamic-linking-class.md)<br/>                                                                                                         | Beschreibt die Verwendung von HLSL-Schnittstellen und-Klassen zum Implementieren dynamischer Verknüpfungen.<br/>                           |
| <span id="Interface_Usage_Restrictions"></span><span id="interface_usage_restrictions"></span><span id="INTERFACE_USAGE_RESTRICTIONS"></span>[Einschränkungen der Schnittstellen Verwendung](overviews-direct3d-11-hlsl-dynamic-linking-expression.md)<br/>                                                                            | Beschreibt Einschränkungen bei der Verwendung von-Schnittstellen im Shader-Code.<br/>                                     |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[HLSL](overviews-direct3d-11-hlsl.md)
</dt> </dl>

 

 





