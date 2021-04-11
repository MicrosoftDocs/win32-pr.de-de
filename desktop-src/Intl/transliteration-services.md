---
description: Die Els-Transliterations Dienste ordnen UTF-16-Text von einem Schreibsystem einem anderen Schreibsystem zu.
ms.assetid: 32e46c52-5c3c-4e22-8f4e-05286ee213ba
title: Transliterations Dienste
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc00b96d56e6b05e70b352c81da0280e9ef35043
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104131736"
---
# <a name="transliteration-services"></a>Transliterations Dienste

Die Els-Transliterations Dienste ordnen UTF-16-Text von einem Schreibsystem einem anderen Schreibsystem zu. Bei jedem Dienst handelt es sich um Daten, die auf einen bestimmten Satz von Eingabe-und Ausgabe-Unicode-Skripts angewendet werden, und die tatsächliche Transliterierung ist intern für die Els-Plattform Die Anwendung kann optional die verfügbaren Dienste für bestimmte Eingabe-und Ausgabe Skripts auflisten und den erforderlichen Dienst auswählen.

Die Plattform verwaltet die Metadaten für die Els-Transliterations Dienste. Die Metadaten für jeden Dienststellen eine Beschreibung des Dienes bereit und listet die Eingabe-und Ausgabe Skripts auf, die der Dienst unterstützt. Die Metadaten werden durch eine [**Mapping \_ Service \_ Info**](/windows/desktop/api/Elscore/ns-elscore-mapping_service_info) -Struktur dargestellt, die von der [**mappinggetservices**](/windows/desktop/api/Elscore/nf-elscore-mappinggetservices) -Funktion abgerufen wird.

## <a name="input-to-a-transliteration-service"></a>Eingabe in einen Transliterations Dienst

Die Eingabe für einen Transliterations Dienst ist UTF-16-Text in einem Schreibsystem.

## <a name="output-of-a-transliteration-service"></a>Ausgabe eines-Transaktions Dienstanbieter

Die Ausgabe eines-Transaktions Dienstanbieter ist UTF-16-Text, der einem zweiten Schreibsystem zugeordnet ist. Wenn keine passende Transaktions Zuordnung für einen bestimmten Teil des Eingabe Texts verfügbar ist, bleibt der Block unverändert.

## <a name="transliteration-service-operation"></a>Vorgang für den Transaktions Dienst

Ein-Transaktions Dienst ordnet Unicode-Text von einem Eingabe Skript nach Bedarf einem Ausgabe Skript zu. Die Anwendung kann den spezifischen zu berücksichtigenden Transaktions Dienst abrufen, indem Sie beim Aufrufen von [**mappinggetservices**](/windows/desktop/api/Elscore/nf-elscore-mappinggetservices)Eingabe-und Ausgabe Skripts angibt oder die Dienst-GUID bereitstellt. Eine weitere Option für die Anwendung besteht darin, alle verfügbaren Transaktionsdienste aufzulisten, indem die Dienst Kategorie "Transliterierung" angegeben wird, wenn **mappinggetservices** aufgerufen wird. In diesem Fall ruft die Anwendung jeden Dienst auf und vergleicht die Ergebnisse mit dem ursprünglichen Text, um festzustellen, ob die Ergebnisse durch den Vorgang eines bestimmten dienstanens geändert wurden.

Die Anwendung kann die Texterkennung für einen Els-Transaktions Dienst mit einem Rückruf von [**mappingrecognizetext**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext)anfordern. Beim Empfang der Anforderung ordnet der-Transaktions Dienst einen Puffer zu, der die Transaktionsdaten enthält, und führt dann eine Texterkennung für jeden Codepunkt in der von der Anwendung bereitgestellten Eingabe Zeichenfolge aus.

> [!Note]  
> Der ursprüngliche Text und der transliterierte Text können eine unterschiedliche Länge aufweisen.

 

## <a name="transliteration-service-guids"></a>Dienst-GUIDs für Transliterationen

Die GUIDs für die-Transliterations Dienste werden in elssrvc. h deklariert, wie im folgenden Code gezeigt.


```C++
// {A3A8333B-F4FC-42f6-A0C4-0462FE7317CB}
static const GUID ELS_GUID_TRANSLITERATION_HANT_TO_HANS =
    { 0xA3A8333B, 0xF4FC, 0x42f6, { 0xA0, 0xC4, 0x04, 0x62, 0xFE, 0x73, 0x17, 0xCB } };

// {3CACCDC8-5590-42dc-9A7B-B5A6B5B3B63B}
static const GUID ELS_GUID_TRANSLITERATION_HANS_TO_HANT =
    { 0x3CACCDC8, 0x5590, 0x42dc, { 0x9A, 0x7B, 0xB5, 0xA6, 0xB5, 0xB3, 0xB6, 0x3B } };

// {D8B983B1-F8BF-4a2b-BCD5-5B5EA20613E1}
static const GUID ELS_GUID_TRANSLITERATION_MALAYALAM_TO_LATIN =
    { 0xD8B983B1, 0xF8BF, 0x4a2b, { 0xBC, 0xD5, 0x5B, 0x5E, 0xA2, 0x06, 0x13, 0xE1 } };

// {C4A4DCFE-2661-4d02-9835-F48187109803}
static const GUID ELS_GUID_TRANSLITERATION_DEVANAGARI_TO_LATIN =
    { 0xC4A4DCFE, 0x2661, 0x4d02, { 0x98, 0x35, 0xF4, 0x81, 0x87, 0x10, 0x98, 0x03 } };

// {3DD12A98-5AFD-4903-A13F-E17E6C0BFE01}
static const GUID ELS_GUID_TRANSLITERATION_CYRILLIC_TO_LATIN =
    { 0x3DD12A98, 0x5AFD, 0x4903, { 0xA1, 0x3F, 0xE1, 0x7E, 0x6C, 0x0B, 0xFE, 0x01 } };

// {F4DFD825-91A4-489f-855E-9AD9BEE55727}
static const GUID ELS_GUID_TRANSLITERATION_BENGALI_TO_LATIN =
    { 0xF4DFD825, 0x91A4, 0x489f, { 0x85, 0x5E, 0x9A, 0xD9, 0xBE, 0xE5, 0x57, 0x27 } };
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zu erweiterten linguistischen Diensten](about-extended-linguistic-services.md)
</dt> </dl>

 

 



