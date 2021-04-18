---
title: Igathernotify init (deprecated)-Methode
description: Dieses Thema der Windows-Desktop Suchschnittstelle ist veraltet und wird durch die Windows Search-isearchpersistentitemschangedsink-API im Windows SDK abgelöst. | Igathernotify init (deprecated)-Methode
ms.assetid: 6a5f89eb-10f4-4262-89bf-b47e345f12eb
keywords:
- Init (veraltet) Methode ältere Windows-Umgebungs Features
- Init (deprecated), ältere Windows-Umgebungs Features, igathernotify-Schnittstelle
- Igathernotify-Schnittstelle ältere Windows-Umgebungs Features, init (deprecated)-Methode
topic_type:
- apiref
api_name:
- IGatherNotify.Init (Deprecated)
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 81379bb4a9a7c6099912bfc9ebca170141d76cd2
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106351883"
---
# <a name="igathernotifyinit-deprecated-method"></a>Igathernotify:: init (deprecated)-Methode

\[**Init** kann in nachfolgenden Versionen des Betriebssystems oder Produkts geändert oder nicht verfügbar sein.\]

Dieses Thema der Windows-Desktop Suchschnittstelle ist veraltet und wird durch die Windows Search- [**isearchpersistentitemschangedsink**](/windows/desktop/api/searchapi/nn-searchapi-isearchpersistentitemschangedsink) -API im Windows SDK abgelöst.

Initialisiert die gathererschnittstelle. Gibt außerdem den zu benachrichtigenden Index und den zu überwachenden Anwendungs Speicher an.

## <a name="syntax"></a>Syntax


```C++
void Init (Deprecated)(
  [in] BSTR    bstrApplication,
  [in] BSTR    bstrProject,
  [in] variant varScopesBstrArray
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*bstrapplikation* \[ in\]
</dt> <dd>

Typ: **BSTR**

Eine Zeichenfolge, die die Zielanwendung angibt.

</dd> <dt>

*bstrinproject* \[ in\]
</dt> <dd>

Typ: **BSTR**

Eine Zeichenfolge, die den Namen des Indexers angibt, an den gathererinformationen übergeben werden sollen.

</dd> <dt>

*varscopesbstrauarray* \[ in\]
</dt> <dd>

Typ: **Variant**

Optionaler Parameter, der es Ihnen ermöglicht, ein Array von Bereichen zu übergeben, die initialisiert werden sollen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Initialisieren Sie mit Application = "rsapp", Project = "myIndex".

 

 
