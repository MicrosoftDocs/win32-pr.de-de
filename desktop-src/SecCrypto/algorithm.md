---
description: Gibt den Algorithmus an, der zum Signieren, umbrechen und Verschlüsseln von Vorgängen verwendet wird.
ms.assetid: 9a3071a3-e62d-43d3-acd7-0685592c78b4
title: Algorithmusobjekt (CAPICOM. h)
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
ms.openlocfilehash: f564efe9df3122951969a45443d58ace60e9db30
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369548"
---
# <a name="algorithm-object"></a>Algorithmusobjekt

\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista, Windows XP. Verwenden Sie stattdessen die [**AlgorithmIdentifier-Klasse**](/dotnet/api/system.security.cryptography.pkcs.algorithmidentifier?view=dotnet-plat-ext-3.1&preserve-view=true) im [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) -Namespace.\]

Das **Algorithmusobjekt** gibt den Algorithmus an, der zum Signieren, umbrechen und Verschlüsseln von Vorgängen verwendet wird.

## <a name="when-to-use"></a>Verwendung

Das **Algorithmusobjekt** wird verwendet, um die folgenden Aufgaben auszuführen:

-   Legen Sie den zu verwendenden Algorithmus fest oder rufen Sie ihn ab.
-   Festlegen oder Abrufen der Schlüssellänge.

> [!Note]  
> CAPICOM versucht, den standardmäßigen Kryptografiedienstanbieter (CSP) des Systems zu verwenden. Wenn dieser CSP den angeforderten Algorithmus oder die Schlüssellänge nicht bereitstellen kann, sucht CAPICOM nach einem verfügbaren von Microsoft bereitgestellten CSP, der den angeforderten Algorithmus und die Schlüssellänge in dieser Verfügbarkeits Reihenfolge verarbeiten kann: Microsoft Enhanced Cryptographic Provider, Microsoft Strong Cryptographic Provider, Microsoft Base Cryptographic Provider.

 

## <a name="members"></a>Member

Das  Algorithmusobjekt verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Das  Algorithmusobjekt verfügt über diese Eigenschaften.



| Eigenschaft                                            | Zugriffstyp           | BESCHREIBUNG                                                                                                                       |
|:----------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------|
| [**KeyLength**](algorithm-keylength.md)<br/> | Lesen/Schreiben<br/> | Legt die Länge des Schlüssels fest oder ruft diese ab.<br/>                                                                               |
| [**Name**](algorithm-name.md)<br/>           | Lesen/Schreiben<br/> | Legt den Algorithmus fest, der zum Signieren, umbrechen und Verschlüsseln von Vorgängen verwendet wird, oder ruft ihn ab. Dies ist die Standard Eigenschaft.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Das  Algorithmusobjekt kann nicht erstellt werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------------|----------------------------------------------------------------------------------------|
| Ende des Supports (Client)<br/> | Windows Vista<br/>                                                               |
| Ende des Supports (Server)<br/> | Windows Server 2008<br/>                                                         |
| Verteilbare Komponente<br/>       | CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP<br/>                  |
| Header<br/>                | <dl> <dt>CAPICOM. h</dt> </dl>   |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Kryptografieobjekte**](cryptography-objects.md)
</dt> </dl>

 

 
