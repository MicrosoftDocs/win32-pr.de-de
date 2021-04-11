---
description: Vorbereiten einer Ressourcen Konfigurationsdatei
ms.assetid: 292b57ea-1c7e-49b6-876c-4ad307a2ec43
title: Vorbereiten einer Ressourcen Konfigurationsdatei
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac162ad7f6d20148e0ef60cb9dc15da41cc27186
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128925"
---
# <a name="preparing-a-resource-configuration-file"></a>Vorbereiten einer Ressourcen Konfigurationsdatei

Sowohl das in den [Ressourcen Dienstprogrammen](resource-utilities.md) beschriebene-Compilerdienstprogramm "muunct" als auch "RC" stellen eine Befehlszeilenoption bereit, mit der Sie eine Ressourcen Konfigurationsdatei für die Basis Sprachen Ressourcen angeben können Die Verwendung dieser öffentlichen, lesbaren XML-Datei ermöglicht mehr Kontrolle über das Aufteilen von Ressourcen, als über die regulären Befehls Zeilenschalter der Hilfsprogramme abgerufen werden können. Auch wenn Sie keine Ressourcen Konfigurationsdatei als Eingabe bereitstellen, enthalten die LN-und sprachspezifischen Ressourcen Dateien Ressourcen Konfigurationsdaten.

Alle Ressourcen Konfigurationsdateien für Win32-Anwendungen beginnen und enden identisch:


```C++
<?xml version="1.0" encoding="utf-8"?> 
<localization>

<resources>
        
        <!-- a single win32Resources element goes here -->

</resources>
</localization>
```



Dieses Thema konzentriert sich auf die Aspekte des XML-Schemas, die beim Entwickeln von nicht verwaltetem Code unter Windows Vista und höher nützlich sind. Insbesondere geht es nur um das Verhalten des win32Resources-Elements.

## <a name="win32resources-element"></a>win32Resources-Element

Das win32Resources-Element verfügt über die in der folgenden Tabelle beschriebenen Attribute.



| Attributname           | Obligatorisch. | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|--------------------------|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| fileType                 | Nein        | Dateityp. Sollte immer "Application" lauten.                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Prüfsumme                 | Nein        | Der Prüfsummen Wert, der in den Ressourcen Konfigurationsdaten der LN-Datei und der sprachspezifischen Ressourcen Dateien angezeigt werden soll. Mit diesem Attribut können Sie z. b. die Prüfsumme aus einer einzelnen sprachspezifischen Ressourcen Datei kopieren, gemäß der Konvention für Englisch (USA), und platzieren Sie die Prüfsumme in einer anderen sprachspezifischen Ressourcen Datei. Die Prüfsumme kann als hexadezimale Zahlen Zeichenfolge angegeben werden, die nicht länger als 32 Zeichen ist. Der numerische Wert muss in eine 128-Bit-Zahl containerbar sein. |
| language                 | Nein        | Die Sprache wird mit einem Namensformat angegeben, das mit RFC 4646 (Windows Vista und höher) kompatibel ist, z. b. "en-US" für Englisch (USA).                                                                                                                                                                                                                                                                                                                                                                             |
| ultimatefallbacklanguage | Nein        | Die Sprache, die in die Ressourcen Konfigurationsdaten für die LN-Datei eingefügt werden soll, und stellt die endgültige Fall Back Sprache dar, die bei einer Suche nach einer entsprechenden sprachspezifischen Ressourcen Datei verwendet werden soll. Wenn das Ressourcen Lade Modul eine angeforderte Ressourcen Datei nicht von den bevorzugten Benutzeroberflächen Sprachen des Threads lädt, wird als letzter Versuch eine ultimative Fall Back Sprache verwendet. Die Sprache wird mit einem Namensformat angegeben, das mit RFC 4646 (Windows Vista und höher) kompatibel ist, z. b. en-US für Englisch (USA).       |
| ultimatefallbacklocation | Nein        | Fall Back Speicherort. Geben Sie "Internal" an, wenn Ultimate-Fall Back Ressourcen in die LN-Datei kompiliert werden. Geben Sie "extern" (Standard) an, wenn die LN-Datei auf eine sprachspezifische Ressourcen Datei für die letzten Fall Back Ressourcen verweisen soll.                                                                                                                                                                                                                                                                                |



 

In der Ressourcen Konfigurationsdatei enthält das win32Resources-Element die untergeordneten Elemente, die in der folgenden Tabelle beschrieben werden.



| Elementname       | BESCHREIBUNG                                                                                                                              |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| Das localizedresources | Ressourcen, die Informationen zu den Ressourcentypen und den einzelnen Ressourcen enthalten, die in einer sprachspezifischen Ressourcen Datei enthalten sind. |
| neutralresources   | Ressourcen, die Informationen zu den in einer LN-Datei enthaltenen Ressourcentypen Kapseln.                                                 |



 

## <a name="localizedresources-element"></a>localizedresources-Element

Lokalisiertes Ressourcen Element. Standardmäßig hat dieses Element keine Attribute und nur einen Typ von Unterelement. Es handelt sich lediglich um einen Container für ResourceType-Elemente.



| Attributname | BESCHREIBUNG                                                                    |
|----------------|--------------------------------------------------------------------------------|
| resourceType   | Der Typ einer einzelnen Ressource, die in einer sprachspezifischen Ressourcen Datei enthalten ist. |



 

## <a name="neutralresources-element"></a>neutralresources-Element

Neutrales Ressourcen Element. Dieses Element ist nur ein Container für ResourceType-Elemente.



| Attributname | BESCHREIBUNG                                        |
|----------------|----------------------------------------------------|
| resourceType   | Der Typ einer einzelnen Ressource, die in einer LN-Datei enthalten ist. |



 

## <a name="resourcetype-element"></a>ResourceType-Element

Das ResourceType-Element kapselt Informationen zu einem einzelnen Ressourcentyp oder einer einzelnen Ressource. Die Attribute sind unten aufgeführt.

> [!Caution]  
> Einige Ressourcen Konfigurationsfehler werden nur durch den RC-Compiler oder muunct abgefangen, abhängig von der Eingabe Ressourcen Datei oder dem Binärdatei Inhalt. Die ResourceType-Fehler in der Ressourcen Konfigurationsdatei, die in der Eingabedatei nicht vorhanden sind, werden nicht abgefangen, was zu unerwartetem Verhalten führt. Benutzer können eine fehlerhafte Ressourcen Konfigurationsdatei verwenden und wissen nicht, bis Sie Binärdateien einführen, die die fehlerhaften Teile der Ressourcen Konfigurationsdatei verwenden. Dadurch wird die Darstellung der Unterbrechungen aus den aktuellen Binärdateien erstellt.

 



| Attributname | Obligatorisch. | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|----------------|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| typameid     | Ja       | Typname oder Bezeichner für die Ressource. Geben Sie einen Zeichen folgen Namen oder eine Zahl an. Wenn eine Zahl verwendet wird, wird der Zeichenfolge ein " \# " vorangestellt, um anzugeben, dass es sich um eine Zahl handelt. Jedes ResourceType-Element darf nur über ein *typenameid* -Attribut verfügen.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| itemName       | Nein        | Die Elementnamen Zeichenfolge für die Ressource, die in der sprachspezifischen Ressourcen Datei abgelegt werden soll. Sie können mehrere Namen angeben, die durch Leerzeichen getrennt sind, z. b. "HTML-MUF-Daten".                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| itemId         | Nein        | Der Bezeichner des einzelnen Ressourcen Elements, das in der sprachspezifischen Ressourcen Datei abgelegt werden soll. Das Element kann als Bereich (z. b. "1-12") oder von einzelnen bezeichlern, getrennt durch Leerzeichen (z. b. "1 3 4"), angegeben werden.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| stringId       | Nein        | Der Zeichen folgen Bezeichner für das einzelne Ressourcen Element, das in die sprachspezifische Ressourcen Datei eingefügt werden soll. Die Zeichenfolge kann als Bereich (z. b. "1-12") oder von einzelnen bezeichlern, getrennt durch Leerzeichen (z. b. "1 3 4"), angegeben werden. Dieses Attribut ermöglicht die Angabe von lokalisierbaren und nicht lokalisierbaren Zeichen folgen Tabellen Einträgen. Er muss in Verbindung mit dem *tytzameid* -Wert "6" verwendet werden, der den Ressourcentyp "String Table Entry" bezeichnet.<br/> Zeichen folgen werden in Blöcken von 16 in einer Zeichen folgen Tabelle gespeichert. Die Zeichen folgen 0 bis 15 werden z. b. in einem einzelnen Ressourcen Element Block gespeichert, und in der Ressourcen Konfigurationsdatei kann als *ItemID* 1 oder als *stringID* "0-15" verwiesen werden. Wenn beispielsweise fünf lokalisierbare Zeichen folgen und drei nicht lokalisierbare Zeichen folgen vorhanden sind, sollten Sie Zeichen folgen Bezeichner 0-4 für die lokalisierbaren Zeichen folgen und Zeichen folgen Bezeichner 16-18 für die nicht lokalisierbaren Zeichen folgen zuweisen. Wenn Sie Zeichen folgen nicht auf diese Weise organisieren, werden die betroffenen Zeichen folgen Blöcke sowohl in der LN-Datei als auch in der sprachspezifischen Ressourcen Datei platziert.<br/> |



 

Wenn Sie die Attribute *ItemName*, *ItemID* und/oder *stringID* für einen bestimmten Ressourcentyp unter dem localizedresource-Element angeben, werden nur die angegebenen Elemente bzw. Zeichen folgen für den angegebenen Ressourcentyp in die sprachspezifische Ressourcen Datei eingefügt. Wenn ein ResourceType-Element ohne einen expliziten Elementnamen, Element Bezeichner oder Zeichen folgen Bezeichner angegeben wird, werden alle Elemente des angegebenen Ressourcentyps in der sprachspezifischen Ressourcen Datei abgelegt. Elemente oder Typen, die nicht in einem localizedresource-Element aufgelistet sind, werden in die LN-Datei eingefügt.

Im folgenden sind die Standard Ressourcentypen und deren numerische Bezeichner aufgeführt:

-   Cursor (1)
-   Bitmap (2)
-   Symbol (3)
-   Menü (4)
-   Dialog (5)
-   Zeichenfolge (6)
-   Fontdir (7)
-   Schriftart (8)
-   Accelerators (9)
-   RCDATA (10)
-   Messagetable (11)
-   Gruppen \_ Cursor (12)
-   Gruppen \_ Symbol (14)
-   Version (16)
-   HTML (23)

## <a name="example"></a>Beispiel


```C++
<?xml version="1.0" encoding="utf-8"?> 
<localization>
  <resources>
    <win32Resources fileType="Application">
      <neutralResources>
        <resourceType
           typeNameId="#16"
        />
      </neutralResources>
      <localizedResources> 
         <resourceType
                typeNameId="#2"
                itemId="5 6 7 8 9 10 11 12"
                itemName="HTML PRI"
         />
         <resourceType
                typeNameId="#4"
         />
         <resourceType
                typeNameId="#5"
         />
         <resourceType
                typeNameId="#6"
         />
         <resourceType
                typeNameId="#9"
         />
         <resourceType
                typeNameId="#11"
         />
         <resourceType
                typeNameId="#16"
         />
         <resourceType
                typeNameId="HTML"
         />
         <resourceType
                typeNameId="#23"
         />
         <resourceType
                typeNameId="#240"
         />
         <resourceType
                typeNameId="#1024"
         />
         <resourceType
                typeNameId="MY_TYPE"
         />
      </localizedResources> 
    </win32Resources>
  </resources>
</localization>
```



## <a name="remarks"></a>Bemerkungen

Wenn Sie ein beliebiges Symbol (3), einen Dialog (5), einen Zeichen folgen-(6) oder einen Versions (16) Ressourcentyp im neutralresources-Element enthalten, müssen Sie diesen Eintrag im localizedresources-Element duplizieren. Sie können dies im obigen Beispiel veranschaulichen, wobei der Ressourcentyp 16 sowohl in neutralen als auch in lokalisierten Ressourcen Abschnitten angezeigt wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vorbereiten von Ressourcen](preparing-resources.md)
</dt> </dl>

 

 




