---
title: Datentypkonvertierungen
description: Datentypkonvertierungen
ms.assetid: 54688ee9-2dd7-466b-b278-13d6f9d1e6ce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8135a3fb86fda9ac9ab9666ec42991a8d04d9e6
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "106342167"
---
# <a name="data-type-conversions"></a>Datentypkonvertierungen

In jeder Programmiersprache werden bestimmte Typen und Container für Daten definiert. Die meisten dieser Datentypen, insbesondere die primitiven, werden problemlos anderen Programmiersprachen zugeordnet. Einige Datentypen haben jedoch keine Entsprechung in einer anderen Sprache und können nicht konvertiert werden.

Spezifische Informationen zu Datentypen, die nicht von ihrer Programmiersprache erkannt werden, finden Sie in den folgenden Themen:

-   [Übersetzen in C++](translating-to-c--.md)
-   [Übersetzen in Visual Basic](translating-to-visual-basic.md)
-   [Übersetzen in Java](translating-to-java.md)

In der folgenden Tabelle sind Konvertierungen zwischen Programmiersprachen für allgemeine Datentypen aufgeführt.



| C++                                     | Visual Basic             | Java                               | Enthält                                                                                       |
|-----------------------------------------|--------------------------|------------------------------------|------------------------------------------------------------------------------------------------|
| **char mit Vorzeichen**<br/>              | Nicht unterstützt<br/> | **byte**<br/>                | 1-Byte-Ganzzahl mit Vorzeichen <br/> (VT \_ I1, \[ T \] )<br/>                                   |
| **unsigned char**<br/>            | **Byte**<br/>      | Nicht unterstützt<br/>           | 1-Byte-Ganzzahl ohne Vorzeichen <br/> (VT \_ UI1, \[ V \] \[ T \] \[ \] \[ s \] )<br/>                 |
| **unsigned char**<br/>            | **Zeichen**<br/> | **char**<br/>                | 2-Byte-Unicode-Zeichen <br/> (VT \_ UI2, \[ T \] \[ P \] )<br/>                          |
| **short**<br/>                    | **Integer**<br/>   | **short**<br/>               | 2-Byte-Ganzzahl mit Vorzeichen <br/> (VT \_ I2, \[ V \] \[ T \] \[ \] \[ s \] )<br/>                    |
| **unsigned short**<br/>           | Nicht unterstützt<br/> | Nicht unterstützt<br/>           | 2-Byte-Ganzzahl ohne Vorzeichen <br/> (VT \_ UI2, \[ T \] \[ P \] )<br/>                           |
| **int**<br/>                      | **Long**<br/>      | **int**<br/>                 | 4-Byte-Ganzzahl mit Vorzeichen <br/> (VT \_ I4, \[ V \] \[ T \] \[ \] \[ s \] )<br/>                    |
| **unsigned int**<br/>             | Nicht unterstützt<br/> | Nicht unterstützt<br/>           | 4-Byte-Ganzzahl ohne Vorzeichen <br/> (VT \_ UI4, \[ T \] \[ P \] )<br/>                           |
| **\_\_Int64**<br/>                | Nicht unterstützt<br/> | **long**<br/>                | 8-Byte-Ganzzahl mit Vorzeichen <br/> (VT \_ I8, \[ T \] \[ P \] )<br/>                              |
| **nicht signiertes \_ \_ Int64**<br/>       | Nicht unterstützt<br/> | Nicht unterstützt<br/>           | 8-Byte-Ganzzahl ohne Vorzeichen <br/> (VT \_ UI8, \[ T \] \[ P \] )<br/>                           |
| **float**<br/>                    | **Single**<br/>    | **float**<br/>               | 4-Byte-Gleit Komma Zahl <br/> (VT \_ R4, \[ V \] \[ T \] \[ \] \[ s \] )<br/>             |
| **double**<br/>                   | **Double**<br/>    | **double**<br/>              | 8-Byte-Gleit Komma Zahl <br/> (VT \_ R8, \[ V \] \[ T \] \[ \] \[ s \] )<br/>             |
| **BSTR**<br/>                     | **String**<br/>    | **Java. lang. String**<br/>    | Automatisierungs Zeichenfolge <br/> (VT \_ BSTR, \[ V \] \[ T \] \[ \] \[ s \] )<br/>                      |
| **BOOL**<br/>                     | **Boolescher Wert**<br/>   | **boolean**<br/>             | Boolean <br/> (VT \_ bool, \[ V \] \[ T \] \[ \] \[ s \] )<br/>                                |
| **Konfigur**<br/>                  | **Konfigur**<br/>   | **com. ms. com. Variant**<br/>  | Variant-weit\* <br/> (VT \_ Variant, \[ V \] \[ T \] \[ \] \[ s \] )<br/>                       |
| [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown)<br/> | **object**<br/>    | **com. ms. com. IUnknown**<br/> | IDispatch-Schnittstellen Zeiger <br/> (VT \_ Dispatch, \[ V \] \[ T \] \[ \] \[ s \] )<br/>        |
| **DATE**<br/>                     | **Datum**<br/>      | **com. ms. com. Variant**<br/>  | Date <br/> (VT \_ Datum, \[ V \] \[ T \] \[ \] \[ s \] )<br/>                                   |
| **CURRENCY**<br/>                 | **Währung**<br/>  | **com. ms. com. Variant**<br/>  | Währung <br/> (VT \_ CY, \[ v \] \[ t \] \[ P \] \[ s \] oder VT \_ Decimal, \[ v \] \[ t \] \[ s \] )<br/> |



 

Weitere Informationen zu VarType-Werten und deren Verwendung finden Sie im Thema [IDispatch-Datentypen und-Strukturen](/previous-versions/ms221600(v=vs.100)).

Die Datentyp Konvertierungen zwischen Skriptsprachen sind einfacher als die für Programmiersprachen. JScript und JavaScript unterstützen beide dieselben Datentypen, und VBScript unterstützt nur einen einzelnen Datentyp ( **Variant**). Folglich werden alle JScript-und JavaScript-Datentypen bei der Konvertierung in VBScript zu **Variant** -Typen. Wenn Sie VBScript in JScript oder JavaScript konvertieren, werden die **Variant** -Typen Zahlen, Zeichen folgen, boolesche Werte usw.

 

