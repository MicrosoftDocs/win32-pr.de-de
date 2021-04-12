---
title: Igathernotify ondatamove (deprecated)-Methode
description: Dieses Thema der Windows-Desktop Suchschnittstelle ist veraltet und wird durch die Windows Search-isearchpersistentitemschangedsink-API im Windows SDK abgelöst. | Igathernotify ondatamove (deprecated)-Methode
ms.assetid: cc223d0f-6508-4e38-b365-c60660db5324
keywords:
- Ondatamove (veraltet) Methode ältere Windows-Umgebungs Features
- Ondatamove (veraltet) Methode ältere Windows-Umgebungs Features, igathernotify-Schnittstelle
- Igathernotify-Schnittstelle ältere Windows-Umgebungs Features, ondatamove (deprecated)-Methode
topic_type:
- apiref
api_name:
- IGatherNotify.OnDataMove (Deprecated)
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9fe38cd11e9072981334e5b724445ea3393d4361
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104353008"
---
# <a name="igathernotifyondatamove-deprecated-method"></a>Igathernotify:: ondatamove (deprecated)-Methode

\[**Ondatamove** kann in nachfolgenden Versionen des Betriebssystems oder Produkts geändert oder nicht verfügbar sein.\]

Dieses Thema der Windows-Desktop Suchschnittstelle ist veraltet und wird durch die Windows Search- [**isearchpersistentitemschangedsink**](/windows/desktop/api/searchapi/nn-searchapi-isearchpersistentitemschangedsink) -API im Windows SDK abgelöst.

Diese Methode benachrichtigt den Indexer von Daten, die verschoben wurden. Wenn die Benachrichtigung an den Indexer gesendet wird, enthält Sie die alte Adresse, die neue Adresse und die logische Adresse.

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

*echangeadvisesemantics* \[ in\]
</dt> <dd>

Type: **Long**

Ein Enumerationsparameter, der den Typ der aufgetretenen Verschiebung beschreibt.

</dd> <dt>

*bstroldaddress* \[ in\]
</dt> <dd>

Typ: **BSTR**

Die alte Adresse des Elements, das verschoben wurde. Für normale Dateien ist *echangeadvisesematics* **null**. Legen Sie für einen Ordner oder ein Verzeichnis *echangeadvisesematics* auf das Verzeichnis der gthr-Zertifizierungsstellen \_ \_ Semantik fest \_ .

</dd> <dt>

*bstrinnewaddress* \[ in\]
</dt> <dd>

Typ: **BSTR**

Die neue Adresse des Elements, das verschoben wurde.

</dd> <dt>

*bstraulogicaladdress* \[ in\]
</dt> <dd>

Typ: **BSTR**

Die logische Adresse des Elements, das verschoben wurde.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

 

 
