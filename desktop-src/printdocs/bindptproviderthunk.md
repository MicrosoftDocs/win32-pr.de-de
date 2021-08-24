---
description: Öffnet eine Instanz eines Druckticketanbieters.
ms.assetid: 815cc360-8dcd-4c58-a64d-5d77436a8623
title: BindPTProviderThunk-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BindPTProviderThunk
api_type:
- DllExport
api_location:
- prntvpt.dll
ms.openlocfilehash: 460728eac742fb96ca122981a5874408e12e6c8eddd36fc901e70874e5e040c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119720230"
---
# <a name="bindptproviderthunk-function"></a>BindPTProviderThunk-Funktion

\[Diese Funktion wird nicht unterstützt und kann in zukünftigen Versionen von Windows deaktiviert oder gelöscht werden. [**PTOpenProviderEx**](/windows/desktop/api/prntvpt/nf-prntvpt-ptopenproviderex) bietet entsprechende Funktionen und sollte stattdessen verwendet werden.\]

Öffnet eine Instanz eines Druckticketanbieters.

## <a name="syntax"></a>Syntax


```C++
HRESULT BindPTProviderThunk(
  _In_  LPTSTR      pszPrinterName,
  _In_  INT         maxVersion,
  _In_  INT         prefVersion,
  _Out_ HPTPROVIDER *phProvider,
  _Out_ INT         *usedVersion
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pszPrinterName* \[ In\]
</dt> <dd>

Der vollständige Name einer Druckwarteschlange.

</dd> <dt>

*maxVersion* \[ In\]
</dt> <dd>

Die neueste Version des [Druckschemas,](./printschema.md) das der Aufrufer unterstützt.

</dd> <dt>

*prefVersion* \[ In\]
</dt> <dd>

Die Vom Aufrufer angeforderte Version des [Druckschemas.](./printschema.md)

</dd> <dt>

*phProvider* \[ out\]
</dt> <dd>

Ein Zeiger auf ein Handle für den Druckticketanbieter.

</dd> <dt>

*usedVersion* \[ out\]
</dt> <dd>

Die Version des [Druckschemas,](./printschema.md) das vom Druckticketanbieter verwendet wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ausgeführt wird, wird **S \_ OK** zurückgegeben. Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben. Weitere Informationen zu COM-Fehlercodes finden Sie unter [Fehlerbehandlung.](../com/error-handling-in-com.md)

## <a name="remarks"></a>Hinweise

Vor dem Aufrufen dieser Funktion muss der aufrufende Thread COM durch Aufrufen von [**CoInitializeEx initialisieren.**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur XP-Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Prntvpt.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Druckschema](./printschema.md)
</dt> <dt>

[**PTOpenProviderEx**](/windows/desktop/api/prntvpt/nf-prntvpt-ptopenproviderex)
</dt> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Druckspooler-API-Funktionen](printing-and-print-spooler-functions.md)
</dt> </dl>

 

