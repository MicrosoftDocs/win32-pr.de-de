---
description: Legt das HCERTSTORE-Handle eines Zertifikat Speicher fest oder ruft es ab.
ms.assetid: 3ff8b4c7-4a9a-4cc1-b0ea-da442ebce157
title: 'Icertstore:: StoreHandle-Eigenschaft'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ICertStore.StoreHandle
- ICertStore.get_StoreHandle
- ICertStore.put_StoreHandle
- CertStore.StoreHandle
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 86f57159a2fdd444f22593ec66fa99510a5260b1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364731"
---
# <a name="icertstorestorehandle-property"></a>Icertstore:: StoreHandle-Eigenschaft

\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP.\]

Die **storeHandle** -Eigenschaft legt das HCERTSTORE-Handle eines Zertifikat Speicher fest oder ruft es ab.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```VB
CertStore.StoreHandle As Long
```



## <a name="property-value"></a>Eigenschaftswert

Das HCERTSTORE-Handle des Zertifikat Speicher.

## <a name="error-codes"></a>Fehlercodes

Wenn die Eigenschaften Zugriffsmethoden **" \_ storeHandle** " und " **\_ storeHandle** " erfolgreich sind, geben Sie "S OK" zurück \_ .

Jeder andere **HRESULT** -Wert gibt an, dass der-Fehler aufgetreten ist.

## <a name="remarks"></a>Bemerkungen

Zum Freigeben des Kontexts muss entweder die [**CloseHandle**](icertstore-closehandle.md) -Methode oder die [**certclosestore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certclosestore) -Funktion aufgerufen werden.

Wenn Sie die **storeHandle** -Eigenschaft festlegen, wird der Status des gesamten [**Speicher**](store.md) Objekts zurückgesetzt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|----------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Icertstore**](icertstore.md)
</dt> </dl>

 

 




