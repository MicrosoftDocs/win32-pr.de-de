---
title: Igathernotify OnDataChange (deprecated)-Methode
description: Dieses Thema der Windows-Desktop Suchschnittstelle ist veraltet und wird durch die Windows Search-isearchpersistentitemschangedsink-API im Windows SDK abgelöst. | Igathernotify OnDataChange (deprecated)-Methode
ms.assetid: 0cbfa6b7-44f0-41f0-93a3-d5941b5822de
keywords:
- OnDataChange (veraltet) Methode ältere Windows-Umgebungs Features
- OnDataChange (veraltet) Methode ältere Windows-Umgebungs Features, igathernotify-Schnittstelle
- Igathernotify-Schnittstelle ältere Windows-Umgebungs Features, OnDataChange (deprecated)-Methode
topic_type:
- apiref
api_name:
- IGatherNotify.OnDataChange (Deprecated)
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d41edeaa591a7f3cbc9494064906af1815597737
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106361156"
---
# <a name="igathernotifyondatachange-deprecated-method"></a>Igathernotify:: OnDataChange (deprecated)-Methode

\[**OnDataChange** kann in nachfolgenden Versionen des Betriebssystems oder Produkts geändert oder nicht verfügbar sein.\]

Dieses Thema der Windows-Desktop Suchschnittstelle ist veraltet und wird durch die Windows Search- [**isearchpersistentitemschangedsink**](/windows/desktop/api/searchapi/nn-searchapi-isearchpersistentitemschangedsink) -API im Windows SDK abgelöst.

Diese Methode benachrichtigt den Indexer von Daten, die sich geändert haben. Beim Senden der Benachrichtigung an den Indexer enthält Sie den Typ der Änderung, die physische Adresse und die logische Adresse.

## <a name="syntax"></a>Syntax


```C++
void OnDataChange (Deprecated)(
  [in] long eChangeAdvise,
  [in] BSTR bstrPhysicalAddress,
  [in] BSTR bstrLogicalAddress
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Echange-Empfehlung* \[ in\]
</dt> <dd>

Type: **Long**

Ein-Enumerationswert, der den Typ der Änderung angibt.

</dd> <dt>

*bstrauphysicaladdress* \[ in\]
</dt> <dd>

Typ: **BSTR**

Die physische Adresse des geänderten Elements.

</dd> <dt>

*bstraulogicaladdress* \[ in\]
</dt> <dd>

Typ: **BSTR**

Die logische Adresse des geänderten Elements.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

 

 
