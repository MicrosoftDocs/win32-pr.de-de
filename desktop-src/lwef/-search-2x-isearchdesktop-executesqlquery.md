---
title: ISearchDesktop ExecuteSQLQuery-Methode
description: Verwendet einen Zeiger auf eine Zeichenfolge, die eine strukturierte Abfragesprache-Abfrage (SQL) und deren Attribute enthält, und gibt einen Zeiger auf den Rückgabesatz zurück.
ms.assetid: df3f473b-0bee-4035-abf8-dbe5249ef0ed
keywords:
- Funktionen der Legacy-Windows ExecuteSQLQuery-Methode
- ExecuteSQLQuery-Methode– Legacy Windows Umgebungsfeatures, ISearchDesktop-Schnittstelle
- ISearchDesktop-Schnittstelle Legacy Windows Umgebungsfeatures, ExecuteSQLQuery-Methode
topic_type:
- apiref
api_name:
- ISearchDesktop.ExecuteSQLQuery
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ec436a427958988e7605673b12b3fd8dc6fd3e1a54ab61cc5f542f0494c34923
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120014290"
---
# <a name="isearchdesktopexecutesqlquery-method"></a>ISearchDesktop::ExecuteSQLQuery-Methode

> [!NOTE]
> Windows Desktop Search 2.x ist eine veraltete Technologie, die ursprünglich als Add-In für Windows XP und Windows Server 2003 verfügbar war. Verwenden Sie in späteren Versionen stattdessen die [Windows Search-API.](../search/-search-reference-entry-page.md) 

Verwendet einen Zeiger auf eine Zeichenfolge, die eine strukturierte Abfragesprache-Abfrage (SQL) und deren Attribute enthält, und gibt einen Zeiger auf den Rückgabesatz zurück.

## <a name="syntax"></a>Syntax


```C++
HRESULT ExecuteSQLQuery(
  [in]  LPCWSTR *pdwAttributes,
  [in]  LPCWSTR pwszURL,
  [out] ppidUrl *ppidUrl
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pdwAttributes* \[ In\]
</dt> <dd>

Typ: **LPCWSTR \***

Eine Zeichenfolge, die die anderen Attribute für die Abfrage enthält.

</dd> <dt>

*pwszURL* \[ In\]
</dt> <dd>

Typ: **LPCWSTR**

Eine Zeichenfolge, die die SQL enthält.

</dd> <dt>

*ppidUrl* \[ out\]
</dt> <dd>

Typ: **ppidUrl \***

Enthält nach erfolgreicher Rückgabe dieser Methode einen Zeiger auf das zurückgegebene Recordset.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Methode erfolgreich ist, wird **S \_ OK zurückgegeben.** Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

 

 




