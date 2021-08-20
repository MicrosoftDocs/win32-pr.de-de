---
description: Vorbereiten einer Ressourcenkonfigurationsdatei
ms.assetid: 292b57ea-1c7e-49b6-876c-4ad307a2ec43
title: Vorbereiten einer Ressourcenkonfigurationsdatei
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b862f48f15997300f079a39de0eb385c535758d9392dc452e1d338d86c8d59e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119147103"
---
# <a name="preparing-a-resource-configuration-file"></a>Vorbereiten einer Ressourcenkonfigurationsdatei

Sowohl die unter [Ressourcen-Hilfsprogramme](resource-utilities.md) beschriebenen UTILITYRCT- als auch rc-Compiler-Hilfsprogramme bieten eine Befehlszeilenoption, mit der Sie eine Ressourcenkonfigurationsdatei für die Ressourcen der Basissprache angeben können. Die Verwendung dieser öffentlichen, lesbaren XML-Datei ermöglicht mehr Kontrolle über die Aufteilung von Ressourcen, als mithilfe der regulären Befehlszeilenschalter der Hilfsprogramme abgerufen werden kann. Auch wenn Sie keine Ressourcenkonfigurationsdatei als Eingabe angeben, enthalten die LN- und sprachspezifischen Ressourcendateien Ressourcenkonfigurationsdaten.

Alle Ressourcenkonfigurationsdateien für Win32-Anwendungen beginnen und enden identisch:


```C++
<?xml version="1.0" encoding="utf-8"?> 
<localization>

<resources>
        
        <!-- a single win32Resources element goes here -->

</resources>
</localization>
```



Dieses Thema konzentriert sich auf die Aspekte des XML-Schemas, die beim Erstellen von nicht verwaltetem Code auf Windows Vista und höher nützlich sind. Insbesondere geht es nur um das Verhalten des win32Resources-Elements.

## <a name="win32resources-element"></a>win32Resources-Element

Das win32Resources-Element verfügt über die in der folgenden Tabelle beschriebenen Attribute.



| Attributname           | Obligatorisch. | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|--------------------------|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| fileType                 | Nein        | Dateityp. Sollte immer "Anwendung" sein.                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Prüfsumme                 | Nein        | Prüfsummenwert, der in den Ressourcenkonfigurationsdaten der LN-Datei und sprachspezifischen Ressourcendateien angezeigt wird. Mit diesem Attribut können Sie z. B. die Prüfsumme aus einer einzelnen sprachspezifischen Ressourcendatei kopieren, gemäß der Konvention für Englisch (USA), und die Prüfsumme in einer anderen sprachspezifischen Ressourcendatei platzieren. Die Prüfsumme kann als hexadezimale Zahlenzeichenfolge angegeben werden, die nicht länger als 32 Zeichen ist. Der numerische Wert muss in einer 128-Bit-Zahl enthalten sein. |
| language                 | Nein        | Sprache, die mit einem Namensformat angegeben wird, das mit RFC 4646 (Windows Vista und höher) kompatibel ist, z. B. en-US für Englisch (USA).                                                                                                                                                                                                                                                                                                                                                                             |
| ultimateFallbackLanguage | Nein        | Sprache zum Einfügen in die Ressourcenkonfigurationsdaten für die LN-Datei, die die endgültige Fallbacksprache darstellt, die bei der Suche nach einer entsprechenden sprachspezifischen Ressourcendatei verwendet werden soll. Wenn das Ressourcenladeprogramm eine angeforderte Ressourcendatei nicht aus den bevorzugten Ui-Sprachen des Threads laden kann, wird als letzter Versuch eine endgültige Fallbacksprache verwendet. Die Sprache wird mit einem Namensformat angegeben, das mit RFC 4646 (Windows Vista und höher) kompatibel ist, z. B. en-US für Englisch (USA).       |
| ultimateFallbackLocation | Nein        | Fallbackspeicherort. Geben Sie "intern" an, wenn endgültige Fallbackressourcen in die LN-Datei kompiliert werden. Geben Sie "external" (Standard) an, wenn die LN-Datei auf eine sprachspezifische Ressourcendatei für die endgültigen Fallbackressourcen verweisen soll.                                                                                                                                                                                                                                                                                |



 

In der Ressourcenkonfigurationsdatei enthält das win32Resources-Element die in der nächsten Tabelle beschriebenen Unterelemente.



| Elementname       | BESCHREIBUNG                                                                                                                              |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| localizedResources | Ressourcen, die Informationen zu den Ressourcentypen und einzelnen Ressourcen kapseln, die in einer sprachspezifischen Ressourcendatei enthalten sind. |
| neutralResources   | Ressourcen, die Informationen zu den in einer LN-Datei enthaltenen Ressourcentypen kapseln.                                                 |



 

## <a name="localizedresources-element"></a>localizedResources-Element

Lokalisiertes Ressourcenelement. Standardmäßig weist dieses Element keine Attribute und nur einen Typ von Untergeordnetem Element auf. Es handelt sich lediglich um einen Container für resourceType-Elemente.



| Attributname | Beschreibung                                                                    |
|----------------|--------------------------------------------------------------------------------|
| resourceType   | Typ einer einzelnen Ressource, die in einer sprachspezifischen Ressourcendatei enthalten ist. |



 

## <a name="neutralresources-element"></a>neutralResources-Element

Neutrales Ressourcenelement. Dieses Element ist nur ein Container für resourceType-Elemente.



| Attributname | Beschreibung                                        |
|----------------|----------------------------------------------------|
| resourceType   | Typ einer einzelnen Ressource, die in einer LN-Datei enthalten ist. |



 

## <a name="resourcetype-element"></a>resourceType-Element

Das resourceType-Element kapselt Informationen zu einem einzelnen Ressourcentyp oder einer einzelnen Ressource. Es enthält die unten aufgeführten Attribute.

> [!Caution]  
> Einige Ressourcenkonfigurationsfehler werden je nach Eingaberessourcendatei oder Binärdateiinhalt nur vom RC-Compiler oder VOM COMPILER ABGEFANGEN. Die resourceType-Fehler in der Ressourcenkonfigurationsdatei, die in der Eingabedatei nicht vorhanden sind, werden nicht abgefangen, was zu unerwartetem Verhalten führt. Benutzer können eine fehlerhafte Ressourcenkonfigurationsdatei verwenden und wissen es erst, wenn sie Binärdateien einführen, die die fehlerhaften Teile der Ressourcenkonfigurationsdatei verwenden, wodurch die Darstellung entsteht, dass die Unterbrechungen aus den aktuellen Binärdateien stammen.

 



| Attributname | Obligatorisch. | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|----------------|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| typeNameId     | Ja       | Geben Sie den Namen oder Bezeichner für die Ressource ein. Geben Sie einen Zeichenfolgennamen oder eine Zahl an. Wenn Sie eine Zahl verwenden, stellen Sie der Zeichenfolge ein \# "" voran, um anzugeben, dass sie eine Zahl darstellt. Jedes resourceType-Element darf nur über ein *typeNameId-Attribut* verfügen.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| itemName       | Nein        | Elementnamenszeichenfolge für die Ressource, die in der sprachspezifischen Ressourcendatei platziert werden soll. Sie können mehrere Namen angeben, die durch Leerzeichen getrennt sind, z. B. "HTML MOFDATA".                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| itemId         | Nein        | Bezeichner des einzelnen Ressourcenelements, das in der sprachspezifischen Ressourcendatei platziert werden soll. Das Element kann als Bereich (z.B. "1-12") oder durch einzelne, durch Leerzeichen getrennte Bezeichner (z.B. "1 3 4") angegeben werden.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| stringId       | Nein        | Zeichenfolgenbezeichner für einzelne Ressourcenelement, die in der sprachspezifischen Ressourcendatei platziert werden sollen. Die Zeichenfolge kann als Bereich (z. B. "1-12") oder durch einzelne Bezeichner angegeben werden, die durch Leerzeichen (z. B. "1 3 4") getrennt sind. Dieses Attribut ermöglicht die Angabe von lokalisierbaren und nicht lokalisierbaren Zeichenfolgentabelleneinträgen. Sie muss in Verbindung mit dem *typeNameId-Wert* "6" verwendet werden, der einen Ressourcentyp für den Eintrag einer Zeichenfolgentabelle anknpft.<br/> Zeichenfolgen werden in Blöcken von 16 in einer Zeichenfolgentabelle gespeichert. Zeichenfolgen 0 bis 15 werden beispielsweise in einem einzelnen Ressourcenelementblock gespeichert und können in der Ressourcenkonfigurationsdatei als *itemId* 1 oder als *stringId* "0-15" referenziert werden. Wenn beispielsweise fünf lokalisierbare Zeichenfolgen und drei nicht lokalisierbare Zeichenfolgen vorhanden sind, sollten Sie zeichenfolgenbezeichner 0-4 für die lokalisierbaren Zeichenfolgen und Zeichenfolgenbezeichner 16-18 für die nicht lokalisierbaren Zeichenfolgen zuweisen. Wenn Sie Zeichenfolgen nicht auf diese Weise organisieren, werden die betroffenen Zeichenfolgenblöcke sowohl in der LN-Datei als auch in der sprachspezifischen Ressourcendatei platziert.<br/> |



 

Wenn Sie die Attribute *itemName,* *itemId* und/oder *stringId* für einen bestimmten Ressourcentyp unter dem localizedResource-Element angeben, werden nur diese angegebenen Elemente oder Zeichenfolgen für den angegebenen Ressourcentyp in der sprachspezifischen Ressourcendatei platziert. Wenn ein resourceType-Element ohne expliziten Elementnamen, Elementbezeichner oder Zeichenfolgenbezeichner angegeben wird, werden alle Elemente des angegebenen Ressourcentyps in der sprachspezifischen Ressourcendatei platziert. Elemente oder Typen, die nicht in einem localizedResource-Element aufgeführt sind, werden in der LN-Datei platziert.

Im Folgenden sind die Standardressourcentypen und ihre numerischen Bezeichner angegeben:

-   CURSOR(1)
-   BITMAP(2)
-   ICON(3)
-   MENU(4)
-   DIALOG(5)
-   STRING(6)
-   FONTDIR(7)
-   FONT(8)
-   ACCELERATORS(9)
-   RCDATA(10)
-   MESSAGETABLE(11)
-   GROUP \_ CURSOR(12)
-   \_GRUPPENSYMBOL(14)
-   VERSION(16)
-   HTML(23)

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



## <a name="remarks"></a>Hinweise

Wenn Sie den Ressourcentyp ICON(3), DIALOG(5), STRING(6) oder VERSION(16) in das neutralResources-Element einfügen, müssen Sie diesen Eintrag im localizedResources-Element duplizieren. Dies wird im obigen Beispiel veranschaulicht, in dem ressourcentyp 16 sowohl in neutralen als auch lokalisierten Ressourcenabschnitten angezeigt wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vorbereiten von Ressourcen](preparing-resources.md)
</dt> </dl>

 

 




