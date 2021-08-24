---
description: Die ELS-Transliterationsdienste ordnen UTF-16-Text von einem Schreibsystem zu einem anderen Schreibsystem zu.
ms.assetid: 32e46c52-5c3c-4e22-8f4e-05286ee213ba
title: Transliteration Services
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d442ed0a9c45d5fb40ffa3f84438f6b2a46ad0a5a6587e3a9fd16dd2f2fd9cff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119788270"
---
# <a name="transliteration-services"></a>Transliteration Services

Die ELS-Transliterationsdienste ordnen UTF-16-Text von einem Schreibsystem zu einem anderen Schreibsystem zu. Bei jedem Dienst handelt es sich tatsächlich um Daten, die auf einen bestimmten Satz von Unicode-Eingabe- und -Ausgabeskripts angewendet werden, und die eigentliche Transliteration ist für die ELS-Plattform intern. Die Anwendung kann optional die verfügbaren Dienste für bestimmte Eingabe- und Ausgabeskripts aufzählen und den gewünschten Dienst auswählen.

Die Plattform verwaltet Metadaten für die ELS-Transliterationsdienste. Metadaten für jeden Dienst enthalten eine Beschreibung des Diensts und listen die Vom Dienst unterstützten Eingabe- und Ausgabeskripts auf. Die Metadaten werden durch eine [**MAPPING \_ SERVICE \_ INFO-Struktur**](/windows/desktop/api/Elscore/ns-elscore-mapping_service_info) dargestellt, die von der [**MappingGetServices-Funktion**](/windows/desktop/api/Elscore/nf-elscore-mappinggetservices) abgerufen wird.

## <a name="input-to-a-transliteration-service"></a>Eingabe für einen Transliterationsdienst

Die Eingabe für einen Transliterationsdienst ist UTF-16-Text in einem Schreibsystem.

## <a name="output-of-a-transliteration-service"></a>Ausgabe eines Transliterationsdiensts

Die Ausgabe eines Transliterationsdiensts ist UTF-16-Text, der einem zweiten Schreibsystem zugeordnet ist. Wenn für einen bestimmten Block des Eingabetexts keine geeignete Transliterationszuordnung verfügbar ist, bleibt der Block unverändert.

## <a name="transliteration-service-operation"></a>Transliterationsdienstvorgang

Ein Transliterationsdienst ordnet Unicode-Text aus einem Eingabeskript einem Ausgabeskript nach Zeichen oder Begriff nach Bedarf zu. Die Anwendung kann den spezifischen gewünschten Transliterationsdienst durch Angeben von Eingabe- und Ausgabeskripts beim Aufrufen von [**MappingGetServices**](/windows/desktop/api/Elscore/nf-elscore-mappinggetservices)oder durch Bereitstellen der Dienst-GUID abrufen. Eine weitere Option für die Anwendung besteht darin, alle verfügbaren Transliterationsdienste aufzuzählen, indem die Dienstkategorie "Transliteration" beim Aufrufen von **MappingGetServices** angegeben wird. In diesem Fall ruft die Anwendung jeden Dienst auf und vergleicht die Ergebnisse mit dem ursprünglichen Text, um festzustellen, ob die Ergebnisse durch den Vorgang eines bestimmten Diensts geändert wurden.

Die Anwendung kann die Texterkennung für einen ELS-Transliterationsdienst mit einem Aufruf von [**MappingRecognizeText**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext)anfordern. Wenn die Anforderung empfangen wird, ordnet der Transliterationsdienst einen Puffer zu, der die transliterierten Daten enthält, und führt dann die Texterkennung für jeden Codepunkt in der von der Anwendung bereitgestellten Eingabezeichenfolge aus.

> [!Note]  
> Der ursprüngliche Text und der transliterierte Text können unterschiedliche Längen aufweisen.

 

## <a name="transliteration-service-guids"></a>GUIDs des Transliterationsdiensts

Die GUIDs für die Transliterationsdienste werden in Elssrvc.h deklariert, wie im folgenden Code gezeigt.


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

 

 



