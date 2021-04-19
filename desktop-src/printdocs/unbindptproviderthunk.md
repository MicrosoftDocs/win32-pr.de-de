---
description: Schließt ein Handle für einen Druck ticketanbieter.
ms.assetid: ce979c89-9f9d-4e89-b142-beed414caa3f
title: Unbindptproviderthunk-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UnbindPTProviderThunk
api_type:
- DllExport
api_location:
- prntvpt.dll
ms.openlocfilehash: dd87f528603624e9957d8c5f3fb12cc857ec4f5a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106363455"
---
# <a name="unbindptproviderthunk-function"></a>Unbindptproviderthunk-Funktion

\[Diese Funktion wird nicht unterstützt und wird in zukünftigen Versionen von Windows möglicherweise deaktiviert oder gelöscht. [**Ptcloseprovider**](/windows/desktop/api/prntvpt/nf-prntvpt-ptcloseprovider) bietet gleichwertige Funktionen und sollte stattdessen verwendet werden.\]

Schließt ein Handle für einen Druck ticketanbieter.

## <a name="syntax"></a>Syntax


```C++
HRESULT UnbindPTProviderThunk(
  _In_ HPTPROVIDER hProvider
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hprovider* \[ in\]
</dt> <dd>

Ein Handle für einen geöffneten Druck ticketanbieter. Dieses Handle wird von der [**bindptproviderthunk**](bindptproviderthunk.md) -Funktion zurückgegeben.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück; andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben. Weitere Informationen zu COM-Fehlercodes finden Sie unter [Fehlerbehandlung](../com/error-handling-in-com.md).

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

[**Ptcloseprovider**](/windows/desktop/api/prntvpt/nf-prntvpt-ptcloseprovider)
</dt> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Druckspooler-API-Funktionen](printing-and-print-spooler-functions.md)
</dt> </dl>

 

