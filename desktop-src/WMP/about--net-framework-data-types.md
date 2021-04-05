---
title: Informationen zu .NET Framework-Datentypen
description: Informationen zu .NET Framework-Datentypen
ms.assetid: 8683888b-889f-4ab2-8eab-dbb79735f13f
keywords:
- Windows Media Player,. NET-Framework
- Windows Media Player-Objektmodell,. NET-Framework
- Objektmodell,. NET-Framework
- Windows Media Player Mobile,. NET-Framework
- Windows Media Player ActiveX-Steuerelement,. NET-Framework
- Windows Media Player Mobile ActiveX-Steuerelement,. NET-Framework
- ActiveX-Steuerelement,. NET-Framework
- .NET Framework, Datentypen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c8774f4ee4521628a05bf766c50c8c7609c1107
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037462"
---
# <a name="about-net-framework-data-types"></a>Informationen zu .NET Framework-Datentypen

Dieser Abschnitt enthält die Informationen, die Sie zum Übersetzen der Skript orientierten Objektmodell Referenz in Microsoft .NET Framework-Basis Datentypen benötigen. Die Windows Media Player Skript Referenz enthält fast alle Informationen, die Sie benötigen, um das Windows Media Player-Steuerelement in einem .NET Framework basierten Programm zu verwenden, und in den meisten Fällen ähnelt die Syntax dem anderer Skriptsprachen, wie z. b. Microsoft JScript.

Die Windows-Media Player Referenz stellt den JScript-Datentyp und ggf. die C++-Konvertierung bereit. Beispielsweise kann eine- **Zahl** von einer-Methode zurückgegeben werden. JScript behandelt alle Zahlen auf die gleiche Weise, aber andere Sprachen unterscheiden zwischen verschiedenen Arten von Zahlen (Integer, Gleit Komma usw.). Der Verweis ermöglicht die C++-Konvertierung für Zahlen Datentypen, da Zahlen von C++ anders verarbeitet werden können. Beispielsweise verwendet C++ den **int** -Datentyp für ganzzahlige Arithmetik und **float** für Gleit Komma Zahlen.

Der .NET Framework verwendet ein geringfügig anderes System von Basis Datentypen. In der folgenden Tabelle sind die Unterschiede in den häufig verwendeten Datentypen aufgeführt. Weitere Informationen zu .NET Framework Basis Datentypen und der Konvertierung in andere Datentyp Systeme finden Sie im .NET Framework Entwicklerhandbuch zu System Namespace-Basis Datentypen.

Diese Tabelle gibt den .NET Framework Klassennamen und den c#-Datentyp an. Datentypen für andere Sprachen werden in den jeweiligen sprach verweisen für jede Sprache definiert.



| Skript Datentyp | C++-Datentyp     | .NET Framework-Klasse (c#-Datentyp) |
|------------------|-------------------|---------------------------------------|
| **Number**       | **int**           | **Int32** (**int**)                   |
| **Number**       | **long**          | **Int32** (**int**)                   |
| **Number**       | **double**        | **Double** (**Double**)               |
| **Number**       | **float**         | **Single** (**float**)                |
| **String**       | **BSTR**          | **String** (**Zeichenfolge**)               |
| **Boolescher Wert**      | **Variant \_ bool** | **Boolean** (**bool**)                |
| **Object**       | **Object**        | **Object** (**Objekt**)               |



 

Wenn Sie Visual Studio verwenden, können Sie die Microsoft IntelliSense-Technologie verwenden, um zu bestimmen, welcher Datentyp für eine bestimmte Funktion erwartet wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Einbetten des Windows Media Player-Steuer Elements in eine .NET Framework Lösung**](using-the-windows-media-player-control-in-a--net-framework-solution.md)
</dt> <dt>

[**Objektmodell Referenz für die Skripterstellung**](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




