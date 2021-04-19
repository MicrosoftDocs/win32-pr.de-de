---
description: Bietet Zugriff auf den Kontext eines CAPICOM X. 509v3-Zertifikat Objekts. In diesem Kontext kann das CAPICOM-Zertifikat in anderen Ableitungen von CryptoAPI verwendet werden.
ms.assetid: 084a3a7b-7523-419f-a504-6fd397030d78
title: Icertcontext-Schnittstelle
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ICertContext
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: f282b97e2257292849a76bc42017e48a95204d01
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352120"
---
# <a name="icertcontext-interface"></a>Icertcontext-Schnittstelle

\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP.\]

Die **icertcontext** -Schnittstelle bietet Zugriff auf den Kontext eines CAPICOM X. 509v3- [**Zertifikat**](certificate.md) Objekts. In diesem Kontext kann das CAPICOM-Zertifikat in anderen Ableitungen von CryptoAPI verwendet werden.

## <a name="when-to-use"></a>Verwendung

Verwenden Sie diese Schnittstelle, wenn Sie in einer anderen Ableitung von CryptoAPI ein CAPICOM- [**Zertifikat**](certificate.md) Objekt verwenden müssen.

## <a name="members"></a>Member

Die **icertcontext** -Schnittstelle verfügt über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **icertcontext** -Schnittstelle verfügt über diese Methoden.



| Methode                                          | BESCHREIBUNG                                                                                                          |
|:------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------|
| [**Freecontext**](icertcontext-freecontext.md) | Gibt einen pccert-kontextfrei, \_ der über die [**certcontext**](icertcontext-certcontext.md) -Eigenschaft abgerufen wurde.<br/> |



 

### <a name="properties"></a>Eigenschaften

Die **icertcontext** -Schnittstelle verfügt über diese Eigenschaften.



| Eigenschaft                                                   | Zugriffstyp           | BESCHREIBUNG                                                        |
|:-----------------------------------------------------------|:----------------------|:-------------------------------------------------------------------|
| [**Certcontext**](icertcontext-certcontext.md)<br/> | Lesen/Schreiben<br/> | Legt den pccert-Kontext eines Zertifikats fest oder ruft ihn ab \_ .<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|----------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



 

 




