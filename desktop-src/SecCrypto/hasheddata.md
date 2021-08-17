---
description: Stellt Funktionen zum Hashing einer Zeichenfolge bereit.
ms.assetid: 893639c2-57b9-48f6-bf60-a21c3368ffeb
title: HashedData-Objekt
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HashedData
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: c61d52e7621acffb76df5bcb05693efb48c695c15e79d1f0a45523a0f0087c6f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119006448"
---
# <a name="hasheddata-object"></a>HashedData-Objekt

\[CAPICOM ist eine nur 32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP. Verwenden Sie stattdessen die [**HashAlgorithm-Klasse**](/previous-versions/windows/) im [**System.Security.Cryptography-Namespace.**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true)\]

Das **HashedData-Objekt** stellt Funktionen zum Hashen einer Zeichenfolge bereit.

## <a name="when-to-use"></a>Verwendung

Das **HashedData-Objekt** wird verwendet, um die folgenden Aufgaben auszuführen:

-   Geben Sie die Inhaltszeichenfolge an, die die zu hashigenden Daten enthält.
-   Wenden Sie einen angegebenen Hashalgorithmus auf die Inhaltszeichenfolge an.

## <a name="members"></a>Member

Das **HashedData-Objekt** verfügt über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Das **HashedData-Objekt** verfügt über diese Methoden.



| Methode                          | Beschreibung                                        |
|:--------------------------------|:---------------------------------------------------|
| [**Hash**](hasheddata-hash.md) | Erstellt einen Hash der angegebenen Zeichenfolge.<br/> |



 

### <a name="properties"></a>Eigenschaften

Das **HashedData-Objekt** verfügt über diese Eigenschaften.



| Eigenschaft                                             | Zugriffstyp           | Beschreibung                                                                                                                                                                          |
|:-----------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Algorithmus**](hasheddata-algorithm.md)<br/> | Lesen/Schreiben<br/> | Legt den Typ des verwendeten Hashalgorithmus fest oder ruft sie ab.<br/>                                                                                                                     |
| [**Wert**](hasheddata-value.md)<br/>         | Schreibgeschützt<br/>  | Ruft die Hashdaten nach erfolgreichen Aufrufen der [**Hashmethode**](hasheddata-hash.md) ab. Der Hash wird im Hexadezimalformat zurückgegeben. Dies ist die Standardeigenschaft.<br/> |



 

## <a name="remarks"></a>Hinweise

Um den Hash einer großen Datenmenge zu erstellen, rufen Sie die [**Hashmethode**](hasheddata-hash.md) für jedes Datenteil auf. Der Hash jedes Datenteils wird mit der [**Value-Eigenschaft**](hasheddata-value.md) verkettet, bis die Eigenschaft gelesen wird. Der Inhalt der **Value-Eigenschaft** wird zurückgesetzt, wenn die Eigenschaft gelesen wird.

Das **HashedData-Objekt** kann erstellt werden und ist für Skripts sicher. Die ProgID für das **HashedData-Objekt** ist "CAPICOM. HashedData.1".

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------------|----------------------------------------------------------------------------------------|
| Ende des Supports (Client)<br/> | Windows Vista<br/>                                                               |
| Ende des Supports (Server)<br/> | Windows Server 2008<br/>                                                         |
| Verteilbare Komponente<br/>       | CAPICOM 2.0 oder höher auf Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
