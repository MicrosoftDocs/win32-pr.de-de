---
description: Gibt den Algorithmus an, der zum Signieren, Umgestalten und Verschlüsseln von Vorgängen verwendet wird.
ms.assetid: 9a3071a3-e62d-43d3-acd7-0685592c78b4
title: Algorithm-Objekt (Capicom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Algorithm
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: b52054c170cd8072bde1b742d0446732fa0b89d2be0dfc2efc66d557cdf98fdb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119880160"
---
# <a name="algorithm-object"></a>Algorithmusobjekt

\[CAPICOM ist eine nur 32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista, Windows XP. Verwenden Sie stattdessen die [**AlgorithmIdentifier-Klasse**](/dotnet/api/system.security.cryptography.pkcs.algorithmidentifier?view=dotnet-plat-ext-3.1&preserve-view=true) im [**System.Security.Cryptography.Pkcs-Namespace.**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true)\]

Das **Algorithm-Objekt** gibt den Algorithmus an, der zum Signieren, Umgestalten und Verschlüsseln von Vorgängen verwendet wird.

## <a name="when-to-use"></a>Verwendung

Das **Algorithm-Objekt** wird verwendet, um die folgenden Aufgaben auszuführen:

-   Legen Sie den zu verwendenden Algorithmus fest, oder rufen Sie diesen ab.
-   Legen Sie die Schlüssellänge fest, oder rufen Sie sie ab.

> [!Note]  
> CAPICOM versucht, den standardmäßigen Kryptografiedienstanbieter (Cryptographic Service Provider, CSP) des Systems zu verwenden. Wenn dieser CSP den angeforderten Algorithmus oder die Schlüssellänge nicht bereitstellen kann, sucht CAPICOM nach einem verfügbaren von Microsoft bereitgestellten CSP, der den angeforderten Algorithmus und die Schlüssellänge in dieser Verfügbarkeitsreihenfolge verarbeiten kann: Microsoft Enhanced Cryptographic Provider, Microsoft Strong Cryptographic Provider, Microsoft Base Cryptographic Provider.

 

## <a name="members"></a>Member

Das **Algorithm-Objekt** verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Das **Algorithm-Objekt** verfügt über diese Eigenschaften.



| Eigenschaft                                            | Zugriffstyp           | BESCHREIBUNG                                                                                                                       |
|:----------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------|
| [**KeyLength**](algorithm-keylength.md)<br/> | Lesen/Schreiben<br/> | Legt die Länge des Schlüssels fest oder ruft sie ab.<br/>                                                                               |
| [**Name**](algorithm-name.md)<br/>           | Lesen/Schreiben<br/> | Legt den Algorithmus fest, der zum Signieren, Umgestalten und Verschlüsseln von Vorgängen verwendet wird, oder ruft den Algorithmus ab. Dies ist die Standardeigenschaft.<br/> |



 

## <a name="remarks"></a>Hinweise

Das **Algorithm-Objekt** kann nicht erstellt werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------------|----------------------------------------------------------------------------------------|
| Ende des Supports (Client)<br/> | Windows Vista<br/>                                                               |
| Ende des Supports (Server)<br/> | Windows Server 2008<br/>                                                         |
| Verteilbare Komponente<br/>       | CAPICOM 2.0 oder höher auf Windows Server 2003 und Windows XP<br/>                  |
| Header<br/>                | <dl> <dt>Capicom.h</dt> </dl>   |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Kryptografieobjekte**](cryptography-objects.md)
</dt> </dl>

 

 
