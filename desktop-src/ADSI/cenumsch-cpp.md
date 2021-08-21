---
title: CENUMSCH. Cpp
description: In der Beispielanbieterkomponente verwendet die Enumeration eines Schemaobjekts die methoden aus cenumsch.cpp, die in der folgenden Tabelle aufgeführt sind.
ms.assetid: edad1ad1-16b9-40f3-b841-a70aa7fff5d9
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08b9be8a58f2d3775f11f85f590f374fc67902a73891484c57e5756645390fda
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117840520"
---
# <a name="cenumschcpp"></a>CENUMSCH. Cpp

In der Beispielanbieterkomponente verwendet die Enumeration eines Schemaobjekts die methoden aus cenumsch.cpp, die in der folgenden Tabelle aufgeführt sind.



| Methode                                        | Beschreibung                                                                                                          |
|-----------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| **CSampleDSSchemaEnum::Create**               | Erstellen Sie ein -Objekt, um die Enumeration eines ADSI-Schemaklassenobjekts zu ermöglichen.                                                |
| **CSampleDSSchemaEnum::CSampleDSSchemaEnum**  | Standardkonstruktor.                                                                                                |
| **CSampleDSSchemaEnum::~CSampleDSSchemaEnum** | Standard-Destruktor.                                                                                                 |
| **CSampleDSSchemaEnum::Next**                 | Rufen Sie die angegebene Anzahl von Elementen aus dem angegebenen Schemaobjekt ab.                                          |
| **CSampleDSSchemaEnum::EnumObjects**          | Verwalten Sie das Abrufen der Schnittstellenze0er auf die Objekte des angegebenen Objekttyps.                               |
| **CSampleDSSchemaEnum::EnumObjects**          | Verwalten Sie das Abrufen der Schnittstellenzeker auf die Objekte des Standardobjekttyps.                                  |
| **CSampleDSSchemaEnum::EnumClasses**          | Verwalten Sie das Abrufen der Schnittstellenzeker nur auf die Schemaklassenobjekte, die in diesem -Objekt enthalten sind.                  |
| **CSampleDSSchemaEnum::GetClassObject**       | Rufen Sie die nächste Schemaklassendefinition ab. Wenn gefunden, erstellen Sie ein Schemaklassenobjekt und geben den Schnittstellenzeiger zurück. |
| **CSampleDSSchemaEnum::EnumProperties**       | Verwalten Sie das Abrufen der Schnittstellenzeker auf die Eigenschaftsobjekte, die nur in diesem -Objekt enthalten sind.                      |
| **CSampleDSSchemaEnum::GetPropertyObject**    | Rufen Sie die nächste Eigenschaftendefinition ab. Wenn gefunden, erstellen Sie ein Schemaklassenobjekt und geben den Schnittstellenzeiger zurück.     |
| **CSampleDSSchemaEnum::EnumSyntaxes**         | Verwalten Sie das Abrufen der Schnittstellenzeker auf die Syntaxobjekte, die nur in diesem -Objekt enthalten sind.                        |
| **CSampleDSSchemaEnum::GetSyntaxObject**      | Rufen Sie die nächste Syntaxdefinition ab. Wenn gefunden, erstellen Sie ein Schemaklassenobjekt und geben den Schnittstellenzeiger zurück.       |



 

 

 




