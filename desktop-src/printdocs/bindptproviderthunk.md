---
description: Öffnet eine Instanz eines Druck Ticket Anbieters.
ms.assetid: 815cc360-8dcd-4c58-a64d-5d77436a8623
title: Bindptproviderthunk-Funktion
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
ms.openlocfilehash: bf63fc6faf9d47993fafb97c8d3a1c18d6d6c985
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215864"
---
# <a name="bindptproviderthunk-function"></a>Bindptproviderthunk-Funktion

\[Diese Funktion wird nicht unterstützt und wird in zukünftigen Versionen von Windows möglicherweise deaktiviert oder gelöscht. [**Ptoperproviderex**](/windows/desktop/api/prntvpt/nf-prntvpt-ptopenproviderex) bietet gleichwertige Funktionen und sollte stattdessen verwendet werden.\]

Öffnet eine Instanz eines Druck Ticket Anbieters.

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

*pszprintername* \[ in\]
</dt> <dd>

Der vollständige Name einer Druck Warteschlange.

</dd> <dt>

*MaxVersion* \[ in\]
</dt> <dd>

Die neueste Version des [Druck Schemas](./printschema.md) , das der Aufrufer unterstützt.

</dd> <dt>

*präfesversion* \[ in\]
</dt> <dd>

Die vom Aufrufer angeforderte Version des [Druck Schemas](./printschema.md) .

</dd> <dt>

*phprovider* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf ein Handle für den Druck ticketanbieter.

</dd> <dt>

*usedversion* \[ vorgenommen\]
</dt> <dd>

Die Version des [Druck Schemas](./printschema.md) , das der Druck ticketanbieter verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück; andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben. Weitere Informationen zu COM-Fehlercodes finden Sie unter [Fehlerbehandlung](../com/error-handling-in-com.md).

## <a name="remarks"></a>Bemerkungen

Vor dem Aufrufen dieser Funktion muss der aufrufenden Thread com durch Aufrufen von [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex)initialisieren.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Prntvpt.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Druck Schema](./printschema.md)
</dt> <dt>

[**Ptopzuproviderex**](/windows/desktop/api/prntvpt/nf-prntvpt-ptopenproviderex)
</dt> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Druckspooler-API-Funktionen](printing-and-print-spooler-functions.md)
</dt> </dl>

 

