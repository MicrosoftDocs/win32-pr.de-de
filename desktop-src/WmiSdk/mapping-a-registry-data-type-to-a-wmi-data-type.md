---
description: Die Anwendung muss die Eigenschaften mit einem Datentyp erstellen, der dem Registrierungs Datentyp zugeordnet ist.
ms.assetid: aa86565c-47eb-40d3-a533-03464cd1c6cd
ms.tgt_platform: multiple
title: Mapping eines Registrierungs Datentyps zu einem WMI-Datentyp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8b96a3bcda0060e376427375059f006e3241118
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529762"
---
# <a name="mapping-a-registry-data-type-to-a-wmi-data-type"></a>Mapping eines Registrierungs Datentyps zu einem WMI-Datentyp

Die Anwendung muss die Eigenschaften mit einem Datentyp erstellen, der dem Registrierungs Datentyp zugeordnet ist. Sie müssen den Registrierungs Datentyp nicht in den Methoden angeben, mit denen Registrierungs Werte erstellt, Get oder festgelegt werden. Der Eingabeparameter, der den Wert enthält, muss jedoch den korrekten WMI-Datentyp aufweisen. Wenn eine Anwendung z. b. **reg \_ DWORD** -Daten aus der Registrierung empfängt, muss die Klasse, die die Daten empfängt, eine **UInt32** -Eigenschaft enthalten.

In der folgenden Tabelle ist die Zuordnung zwischen der Registrierung und den WMI-Datentypen aufgeführt, die in den [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) -Methoden verwendet werden.



| Registrierungs Datentyp      | WMI-Datentyp                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|-------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **REG- \_ Binärdatei**         | **Uint8** -Array<br/> Ein Array von Werten, die nicht größer als 255 oder HEX FF sind. Der folgende Visual Basic Skriptcode erstellt z. b. ein Array, das diesem Datentyp entspricht.<br/> `BinArray = Array(&H01, &Ha2)`<br/> Die [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) -Klassenmethode [**SetBinaryValue**](/previous-versions/windows/desktop/regprov/setbinaryvalue-method-in-class-stdregprov) erfordert **den \_ binären** Datentyp reg.<br/>                                                                                          |
| **REG \_ DWORD**          | **UInt32**, **sint32** oder Visual Basic **Ganzzahl**<br/> Ein einzelner 32-Bit-Wert. Die [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) -Klassen Methoden [**GetDWORDValue**](/previous-versions/windows/desktop/regprov/getdwordvalue-method-in-class-stdregprov) und [**SetDWORDValue**](/previous-versions/windows/desktop/regprov/setdwordvalue-method-in-class-stdregprov) erfordern den **reg \_ DWORD** -Datentyp.<br/>                                                                                                                                                                  |
| **REG- \_ SZ**             | **string**<br/> Die [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) -Klassenmethode [**SetStringValue**](/previous-versions/windows/desktop/regprov/setstringvalue-method-in-class-stdregprov) erfordert den **reg \_ SZ** -Datentyp.<br/>                                                                                                                                                                                                                                                                                                            |
| **REG \_ QWORD**          | **UInt64**.<br/> Ein einzelner 64-Bit-Wert. Die [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) -Klassen Methoden [**GetQWORDValue**](/previous-versions/windows/desktop/regprov/getqwordvalue-method-in-class-stdregprov) und [**SetQWORDValue**](/previous-versions/windows/desktop/regprov/setqwordvalue-method-in-class-stdregprov) erfordern den **reg \_ QWORD** -Datentyp.<br/>                                                                                                                                                                                                         |
| **REG \_ Expand \_ SZ**     | **string**<br/> Erweiterte Zeichen folgen sind spezielle Zeichen folgen, die System Umgebungsvariablen darstellen. Beispielsweise wird mit dem folgenden VBScript-Code eine Zeichenfolge erstellt, die die **lokale HKEY- \_ \_ Benutzer** Umgebungsvariable TEMP darstellt.<br/> `TEMP = "%USERPROFILE\LocalSettings\Temp%"`<br/> Die [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) -Klassenmethode [**SetExpandedStringValue**](/previous-versions/windows/desktop/regprov/setexpandedstringvalue-method-in-class-stdregprov) erfordert den **reg \_ Expand \_ SZ** -Datentyp.<br/> |
| **REG \_ \_ MultiSZ**      | **Zeichen** folgen Array<br/> Der MultiString-Datentyp enthält mehrere Zeichen folgen. Der folgende VBScript-Code erstellt beispielsweise ein Array, das diesem Datentyp entspricht.<br/> `MultiValue = Array("first", "second", "third")`<br/> Die [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) -Klassenmethode [**SetMultiStringValue**](/previous-versions/windows/desktop/regprov/setmultistringvalue-method-in-class-stdregprov) erfordert **den \_ reg \_ MultiSZ** -Datentyp.<br/>                                                                     |
| **REG- \_ Ressourcen \_ Liste** | Gegebenenfalls. Weitere Informationen finden Sie unter [beschreiben einer Ressource für die Registrierung](describing-a-resource-for-the-registry.md).<br/>                                                                                                                                                                                                                                                                                                                                                                    |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Definieren von Klassen für den System Registrierungs Anbieter](defining-classes-for-the-system-registry-provider.md)
</dt> </dl>

 

