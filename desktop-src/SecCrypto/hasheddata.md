---
description: Stellt Funktionen für das hashte einer Zeichenfolge bereit.
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
ms.openlocfilehash: b6e54d7d2ca52ceafe500615af4063dfc7310b0d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356360"
---
# <a name="hasheddata-object"></a>HashedData-Objekt

\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP. Verwenden Sie stattdessen die [**HashAlgorithm-Klasse**](/previous-versions/windows/) im [**System. Security. Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) -Namespace.\]

Das **hashedData** -Objekt stellt Funktionen zum Hashwert einer Zeichenfolge bereit.

## <a name="when-to-use"></a>Verwendung

Das **hashedData** -Objekt wird verwendet, um die folgenden Aufgaben auszuführen:

-   Geben Sie die Inhalts Zeichenfolge an, die die zu hashenden Daten enthält.
-   Wendet einen angegebenen Hash Algorithmus auf die Inhalts Zeichenfolge an.

## <a name="members"></a>Member

Das **hashedData** -Objekt verfügt über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Das **hashedData** -Objekt verfügt über diese Methoden.



| Methode                          | BESCHREIBUNG                                        |
|:--------------------------------|:---------------------------------------------------|
| [**Hash**](hasheddata-hash.md) | Erstellt einen Hash der angegebenen Zeichenfolge.<br/> |



 

### <a name="properties"></a>Eigenschaften

Das **hashedData** -Objekt verfügt über diese Eigenschaften.



| Eigenschaft                                             | Zugriffstyp           | BESCHREIBUNG                                                                                                                                                                          |
|:-----------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Algorithmus**](hasheddata-algorithm.md)<br/> | Lesen/Schreiben<br/> | Legt den Typ des verwendeten Hash Algorithmus fest oder ruft ihn ab.<br/>                                                                                                                     |
| [**Wert**](hasheddata-value.md)<br/>         | Schreibgeschützt<br/>  | Ruft die Hash Daten nach erfolgreichen Aufrufen der [**Hash**](hasheddata-hash.md) Methode ab. Der Hash wird im Hexadezimal Format zurückgegeben. Dies ist die Standard Eigenschaft.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Um den Hash einer großen Datenmenge zu erstellen, rufen Sie die [**Hash**](hasheddata-hash.md) Methode für jedes Datenelement auf. Der Hash der einzelnen Daten Daten wird bis zum Lesen der Eigenschaft mit der [**value**](hasheddata-value.md) -Eigenschaft verkettet. Der Inhalt der **value** -Eigenschaft wird zurückgesetzt, wenn die Eigenschaft gelesen wird.

Das **hashedData** -Objekt kann erstellt und ist für die Skripterstellung sicher. Die ProgID für das **hashedData** -Objekt ist "CAPICOM". HashedData. 1 ".

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------------|----------------------------------------------------------------------------------------|
| Ende des Supports (Client)<br/> | Windows Vista<br/>                                                               |
| Ende des Supports (Server)<br/> | Windows Server 2008<br/>                                                         |
| Verteilbare Komponente<br/>       | CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
