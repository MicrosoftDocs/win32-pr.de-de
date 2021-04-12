---
title: Igathernotify addscope (deprecated)-Methode
description: Dieses Thema der Windows-Desktop Suchschnittstelle ist veraltet und wird durch die Windows Search-isearchpersistentitemschangedsink-API im Windows SDK abgelöst. | Igathernotify addscope (deprecated)-Methode
ms.assetid: 3b250818-1876-40b2-9a85-91f2bf6f52ec
keywords:
- Addscope (veraltet) Methode Legacy-Windows-Umgebungs Features
- Addscope (veraltet) Methode Legacy-Windows-Umgebungs Features, igathernotify-Schnittstelle
- Igathernotify-Schnittstelle ältere Windows-Umgebungs Features, addscope (deprecated)-Methode
topic_type:
- apiref
api_name:
- IGatherNotify.AddScope (Deprecated)
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 967dc4f30acee2f8d8adbcfec04f0508e53bba15
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104353009"
---
# <a name="igathernotifyaddscope-deprecated-method"></a>Igathernotify:: addscope (deprecated)-Methode

\[**Addscope** kann in nachfolgenden Versionen des Betriebssystems oder Produkts geändert werden oder nicht verfügbar sein.\]

Dieses Thema der Windows-Desktop Suchschnittstelle ist veraltet und wird durch die Windows Search- [**isearchpersistentitemschangedsink**](/windows/desktop/api/searchapi/nn-searchapi-isearchpersistentitemschangedsink) -API im Windows SDK abgelöst.

Fügt die Startseite oder die URL hinzu, die Sie überwachen. Dadurch wird eine inkrementelle durch Forstung initiiert, wenn eine Verbindung hergestellt wird

## <a name="syntax"></a>Syntax


```C++
void AddScope (Deprecated)(
  [in] BSTR bstrScope
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*bstrauscope* \[ in\]
</dt> <dd>

Typ: **BSTR**

Eine Zeichenfolge, die die zu überwachende Startseite oder den zu überwachenden urlangibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Beim Aufrufen dieser Methode wird ein inkrementelles Crawl gestartet, wenn eine Verbindung mit dem Speicher Danach wird davon ausgegangen, dass alle URL-Änderungen nach dem ersten Update durch eine Benachrichtigung erfolgen.

 

 
