---
description: Die Anwendung muss die Eigenschaften mit einem Datentyp erstellen, der dem Registrierungsdatentyp zugeordnet ist.
ms.assetid: aa86565c-47eb-40d3-a533-03464cd1c6cd
ms.tgt_platform: multiple
title: Zuordnen eines Registrierungsdatentyps zu einem WMI-Datentyp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e620d51eee52592df946e822165d8ed1833214c6f75519d4274b0d7fe3f5550c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119050688"
---
# <a name="mapping-a-registry-data-type-to-a-wmi-data-type"></a>Zuordnen eines Registrierungsdatentyps zu einem WMI-Datentyp

Die Anwendung muss die Eigenschaften mit einem Datentyp erstellen, der dem Registrierungsdatentyp zugeordnet ist. Sie müssen den Registrierungsdatentyp nicht in den Methoden angeben, die Registrierungswerte erstellen, abrufen oder festlegen. Der Eingabeparameter, der den Wert enthält, muss jedoch den richtigen WMI-Datentyp aufweisen. Wenn eine Anwendung beispielsweise **REG \_ DWORD-Daten** aus der Registrierung empfängt, muss die Klasse, die die Daten empfängt, eine **Uint32-Eigenschaft** enthalten.

In der folgenden Tabelle ist die Zuordnung zwischen registrierungs- und WMI-Datentypen aufgeführt, die in den [**StdRegProv-Methoden**](/previous-versions/windows/desktop/regprov/stdregprov) verwendet werden.



| Registrierungsdatentyp      | WMI-Datentyp                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|-------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **REG \_ BINARY**         | **uint8-Array**<br/> Ein Array von Werten, die 255 oder hexadezimale FF nicht überschreiten. Mit dem folgenden Visual Basic Skriptcode wird beispielsweise ein Array erstellt, das diesem Datentyp entspricht.<br/> `BinArray = Array(&H01, &Ha2)`<br/> Die [**StdRegProv-Klassenmethode**](/previous-versions/windows/desktop/regprov/stdregprov) [**SetBinaryValue**](/previous-versions/windows/desktop/regprov/setbinaryvalue-method-in-class-stdregprov) erfordert den **REG \_ BINARY-Datentyp.**<br/>                                                                                          |
| **REG \_ DWORD**          | **uint32,** **sint32** oder Visual Basic **integer**<br/> Ein einzelner 32-Bit-Wert. Die [**StdRegProv-Klassenmethoden**](/previous-versions/windows/desktop/regprov/stdregprov) [**GetDWORDValue**](/previous-versions/windows/desktop/regprov/getdwordvalue-method-in-class-stdregprov) und [**SetDWORDValue**](/previous-versions/windows/desktop/regprov/setdwordvalue-method-in-class-stdregprov) erfordern den **REG \_ DWORD-Datentyp.**<br/>                                                                                                                                                                  |
| **REG \_ SZ**             | **string**<br/> Die [**StdRegProv-Klassenmethode**](/previous-versions/windows/desktop/regprov/stdregprov) [**SetStringValue**](/previous-versions/windows/desktop/regprov/setstringvalue-method-in-class-stdregprov) erfordert den **REG \_ SZ-Datentyp.**<br/>                                                                                                                                                                                                                                                                                                            |
| **REG \_ QWORD**          | **uint64**.<br/> Ein einzelner 64-Bit-Wert. Die [**StdRegProv-Klassenmethoden**](/previous-versions/windows/desktop/regprov/stdregprov) [**GetQWORDValue**](/previous-versions/windows/desktop/regprov/getqwordvalue-method-in-class-stdregprov) und [**SetQWORDValue**](/previous-versions/windows/desktop/regprov/setqwordvalue-method-in-class-stdregprov) erfordern den **REG \_ QWORD-Datentyp.**<br/>                                                                                                                                                                                                         |
| **REG \_ EXPAND \_ SZ**     | **string**<br/> Erweiterte Zeichenfolgen sind spezielle Zeichenfolgen, die Systemumgebungsvariablen darstellen. Der folgende VBScript-Code erstellt beispielsweise eine Zeichenfolge, die die **HKEY \_ LOCAL USER-Umgebungsvariable \_** TEMP darstellt.<br/> `TEMP = "%USERPROFILE\LocalSettings\Temp%"`<br/> Die [**StdRegProv-Klassenmethode**](/previous-versions/windows/desktop/regprov/stdregprov) [**SetExpandedStringValue**](/previous-versions/windows/desktop/regprov/setexpandedstringvalue-method-in-class-stdregprov) erfordert den **REG EXPAND \_ \_ SZ-Datentyp.**<br/> |
| **REG \_ MULTI \_ SZ**      | **Zeichenfolgenarray**<br/> Der Multistring-Datentyp enthält mehrere Zeichenfolgen. Der folgende VBScript-Code erstellt beispielsweise ein Array, das zu diesem Datentyp passt.<br/> `MultiValue = Array("first", "second", "third")`<br/> Die [**StdRegProv-Klassenmethode**](/previous-versions/windows/desktop/regprov/stdregprov) [**SetMultiStringValue**](/previous-versions/windows/desktop/regprov/setmultistringvalue-method-in-class-stdregprov) erfordert den **REG MULTI \_ \_ SZ-Datentyp.**<br/>                                                                     |
| **\_ \_ REG-RESSOURCENLISTE** | Gegebenenfalls. Weitere Informationen finden Sie unter [Beschreiben einer Ressource für die Registrierung.](describing-a-resource-for-the-registry.md)<br/>                                                                                                                                                                                                                                                                                                                                                                    |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Definieren von Klassen für den Systemregistrierungsanbieter](defining-classes-for-the-system-registry-provider.md)
</dt> </dl>

 

