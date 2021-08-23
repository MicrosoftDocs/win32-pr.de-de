---
title: IGatherNotify OnDataMove-Methode (veraltet)
description: Dieses Windows-Benutzeroberflächenthema für die Desktopsuche ist veraltet und wird durch die Windows Search ISearchPersistentItemsChangedSink-API im Windows SDK ersetzt. | IGatherNotify OnDataMove-Methode (veraltet)
ms.assetid: cc223d0f-6508-4e38-b365-c60660db5324
keywords:
- OnDataMove-Methode (veraltet) Legacy-Windows-Umgebungsfeatures
- OnDataMove-Methode (veraltet) Legacy-Windows Umgebungsfeatures, IGatherNotify-Schnittstelle
- IGatherNotify interface Legacy Windows Environment Features , OnDataMove (Veraltet)-Methode
topic_type:
- apiref
api_name:
- IGatherNotify.OnDataMove (Deprecated)
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2f3d4f7d91bc9e9741f227812997a820ab4180ccf438d52ae8cfea93f67dc0bf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119665870"
---
# <a name="igathernotifyondatamove-deprecated-method"></a>IGatherNotify::OnDataMove -Methode (veraltet)

\[**OnDataMove** kann in nachfolgenden Versionen des Betriebssystems oder Produkts geändert oder nicht verfügbar sein.\]

Dieses Windows-Benutzeroberflächenthema für die Desktopsuche ist veraltet und wird durch die Windows Search [**ISearchPersistentItemsChangedSink-API**](/windows/desktop/api/searchapi/nn-searchapi-isearchpersistentitemschangedsink) im Windows SDK ersetzt.

Diese Methode benachrichtigt den Indexer über daten, die verschoben wurden. Wenn die Benachrichtigung an den Indexer gesendet wird, enthält sie die alte Adresse, die neue Adresse und die logische Adresse.

## <a name="syntax"></a>Syntax


```C++
void OnDataMove (Deprecated)(
  [in] long eChangeAdviseSemantics,
  [in] BSTR bstrOldAddress,
  [in] BSTR bstrNewAddress,
  [in] BSTR bstrLogicalAddress
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*eChangeAdviseSemantics* \[ In\]
</dt> <dd>

Typ: **long**

Ein aufzählter Parameter, der den Typ der aufgetretenen Bewegung beschreibt.

</dd> <dt>

*bstrOldAddress* \[ In\]
</dt> <dd>

Typ: **BSTR**

Die alte Adresse des Elements, das verschoben wurde. Für normale Dateien ist *eChangeAdviseSematics* **NULL.** Legen Sie für einen Ordner oder ein Verzeichnis *eChangeAdviseSematics auf* GTHR \_ CA \_ SEMANTICS DIRECTORY \_ fest.

</dd> <dt>

*bstrNewAddress* \[ In\]
</dt> <dd>

Typ: **BSTR**

Die neue Adresse des Elements, das verschoben wurde.

</dd> <dt>

*bstrLogicalAddress* \[ In\]
</dt> <dd>

Typ: **BSTR**

Die logische Adresse des Elements, das verschoben wurde.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

 

 
