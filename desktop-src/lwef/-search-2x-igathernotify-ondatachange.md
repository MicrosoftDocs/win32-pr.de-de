---
title: IGatherNotify OnDataChange-Methode (veraltet)
description: Dieses Windows-Benutzeroberflächenthema für die Desktopsuche ist veraltet und wird durch die Windows Search ISearchPersistentItemsChangedSink-API im Windows SDK ersetzt. | IGatherNotify OnDataChange-Methode (veraltet)
ms.assetid: 0cbfa6b7-44f0-41f0-93a3-d5941b5822de
keywords:
- OnDataChange-Methode (veraltet) – Legacy-Windows-Umgebungsfeatures
- OnDataChange-Methode (veraltet) Legacy-Windows Environment Features, IGatherNotify-Schnittstelle
- IGatherNotify interface Legacy Windows Environment Features , OnDataChange (Veraltet) method (IGatherNotify interface Legacy Windows Environment Features , OnDataChange (Veraltet)-Methode
topic_type:
- apiref
api_name:
- IGatherNotify.OnDataChange (Deprecated)
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 95533a7937136a0f828a292efe7e398258e3c880974e031d9d7d2797f721f2a6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118481594"
---
# <a name="igathernotifyondatachange-deprecated-method"></a>IGatherNotify::OnDataChange-Methode (veraltet)

\[**OnDataChange** kann in nachfolgenden Versionen des Betriebssystems oder Produkts geändert oder nicht verfügbar sein.\]

Dieses Windows-Benutzeroberflächenthema für die Desktopsuche ist veraltet und wird durch die Windows Search [**ISearchPersistentItemsChangedSink-API**](/windows/desktop/api/searchapi/nn-searchapi-isearchpersistentitemschangedsink) im Windows SDK ersetzt.

Diese Methode benachrichtigt den Indexer über geänderte Daten. Wenn die Benachrichtigung an den Indexer gesendet wird, enthält sie den Typ der Änderung, die physische Adresse und die logische Adresse.

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

*eChangeAdvise* \[ In\]
</dt> <dd>

Typ: **long**

Ein aufzählter Wert, der den Typ der Änderung angibt.

</dd> <dt>

*bstrPhysicalAddress* \[ In\]
</dt> <dd>

Typ: **BSTR**

Die physische Adresse des geänderten Elements.

</dd> <dt>

*bstrLogicalAddress* \[ In\]
</dt> <dd>

Typ: **BSTR**

Die logische Adresse des geänderten Elements.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

 

 
