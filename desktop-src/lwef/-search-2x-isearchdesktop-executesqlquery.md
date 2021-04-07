---
title: ISearchDesktop ExecuteSQLQuery-Methode
description: Nimmt einen Zeiger auf eine Zeichenfolge, die eine Structured Query Language (SQL)-Abfrage und deren Attribute enthält, und gibt einen Zeiger auf die Rückgabe Menge zurück.
ms.assetid: df3f473b-0bee-4035-abf8-dbe5249ef0ed
keywords:
- ExecuteSQLQuery-Methode ältere Windows-Umgebungs Features
- ExecuteSQLQuery-Methode Legacy-Windows-Umgebungs Features, ISearchDesktop-Schnittstelle
- ISearchDesktop Interface, ältere Windows-Umgebungs Funktionen, ExecuteSQLQuery-Methode
topic_type:
- apiref
api_name:
- ISearchDesktop.ExecuteSQLQuery
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f0b13ff361d07f99efe1366e2201d610eac10523
ms.sourcegitcommit: b9a94cea8f83153214af4c09509e1cc61a1bb616
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/19/2020
ms.locfileid: "103724011"
---
# <a name="isearchdesktopexecutesqlquery-method"></a>ISearchDesktop:: ExecuteSQLQuery-Methode

> [!NOTE]
> Windows-Desktop Suche 2. x ist eine veraltete Technologie, die ursprünglich als Add-in für Windows XP und Windows Server 2003 verfügbar war. Verwenden Sie in späteren Versionen stattdessen die [Windows Search-API](../search/-search-reference-entry-page.md) . 

Nimmt einen Zeiger auf eine Zeichenfolge, die eine Structured Query Language (SQL)-Abfrage und deren Attribute enthält, und gibt einen Zeiger auf die Rückgabe Menge zurück.

## <a name="syntax"></a>Syntax


```C++
HRESULT ExecuteSQLQuery(
  [in]  LPCWSTR *pdwAttributes,
  [in]  LPCWSTR pwszURL,
  [out] ppidUrl *ppidUrl
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pdwattributes* \[ in\]
</dt> <dd>

Typ: **LPCWSTR \***

Eine Zeichenfolge, die die anderen Attribute für die Abfrage enthält.

</dd> <dt>

*pwszurl* \[ in\]
</dt> <dd>

Typ: **LPCWSTR**

Eine Zeichenfolge, die die SQL-Abfrage enthält.

</dd> <dt>

*ppidurl* \[ vorgenommen\]
</dt> <dd>

Typ: **ppidurl \***

Wenn diese Methode erfolgreich zurückgegeben wird, enthält Sie einen Zeiger auf das zurückgegebene Recordset.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

 

 




