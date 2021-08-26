---
title: Informationen .NET Framework Datentypen
description: Informationen .NET Framework Datentypen
ms.assetid: 8683888b-889f-4ab2-8eab-dbb79735f13f
keywords:
- Windows Media Player,.NET Framework
- Windows Media Player Objektmodell,.NET Framework
- Objektmodell,.NET Framework
- Windows Media Player Mobile,.NET Framework
- Windows Media Player ActiveX,.NET Framework
- Windows Media Player Mobile ActiveX-Steuerelement,.NET Framework
- ActiveX,.NET Framework
- .NET Framework,Datentypen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36854d971b0fc220f8f77b754b08b486ff93d339935bedcf33edca39fb701e4d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120004519"
---
# <a name="about-net-framework-data-types"></a>Informationen .NET Framework Datentypen

Dieser Abschnitt enthält die Informationen, die Sie benötigen, um die skriptorientierte Objektmodellreferenz in Microsoft .NET Framework-Basisdatentypen zu übersetzen. Die Windows Media Player-Skriptreferenz enthält fast alle Informationen, die Sie benötigen, um das Windows Media Player-Steuerelement in einem .NET Framework-basierten Programm zu verwenden. In den meisten Fällen ähnelt die Syntax der Syntax anderer Skriptsprachen wie Microsoft JScript.

Der Windows Media Player enthält den JScript datentyp und bei Bedarf die C++-Konvertierung. Beispielsweise kann eine **Zahl** von einer Methode zurückgegeben werden. JScript behandelt alle Zahlen auf die gleiche Weise, aber andere Sprachen unterscheiden zwischen verschiedenen Zahlentypen (ganze Zahl, Gleitkommazahl und so weiter). Der Verweis gibt die C++-Konvertierung für Zahlendatentypen an, da Zahlen von C++ unterschiedlich verarbeitet werden können. C++ verwendet z. B. den **datentyp int** für die ganzzahlige Arithmetik und **float für** Gleitkommawerte.

Die .NET Framework verwendet ein etwas anderes System von Basisdatentypen. Die folgende Tabelle zeigt die Unterschiede in den gängigen Datentypen, die Sie wahrscheinlich verwenden werden. Weitere Informationen zu .NET Framework Basisdatentypen und zur Konvertierung in andere Datentypsysteme finden Sie im .NET Framework Developer es Guide discussion of System Namespace base data types (Entwicklerhandbuch zu Basisdatentypen für Systemnamespaces).

Diese Tabelle enthält den .NET Framework Klassennamen und den C#-Datentyp. Datentypen für andere Sprachen werden für jede Sprache in ihren jeweiligen Sprachverweisen definiert.



| Skriptdatentyp | C++-Datentyp     | .NET Framework -Klasse (C#-Datentyp ) |
|------------------|-------------------|---------------------------------------|
| **Number**       | **int**           | **Int32** (**int**)                   |
| **Number**       | **long**          | **Int32** (**int**)                   |
| **Number**       | **double**        | **Double** (**double**)               |
| **Number**       | **float**         | **Single** (**float**)                |
| **String**       | **Bstr**          | **String** (**string**)               |
| **Boolean**      | **VARIANT \_ BOOL** | **Boolean** (**bool**)                |
| **Object**       | **Object**        | **Object** (**object**)               |



 

Wenn Sie Visual Studio verwenden, können Sie die Microsoft IntelliSense-Technologie verwenden, um zu bestimmen, welcher Datentyp für eine bestimmte Funktion erwartet wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Einbetten des Windows Media Player-Steuerelements in eine .NET Framework Projektmappe**](using-the-windows-media-player-control-in-a--net-framework-solution.md)
</dt> <dt>

[**Objektmodellreferenz für die Skripterstellung**](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




