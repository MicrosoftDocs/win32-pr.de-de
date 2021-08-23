---
title: sh_job-Schlüsselwort
description: Das Schlüsselwort \sh \_ job\ gibt an, dass das Systemobjekt ein Handle für einen Auftrag ist.
keywords:
- sh_job MIDL-Schlüsselwort
topic_type:
- apiref
api_name:
- sh_job
api_type:
- NA
ms.topic: reference
ms.date: 02/05/2021
ms.openlocfilehash: dd71db0310b450db1d9c87879e8ac10ad998d1d21e48a60eb9d816c0a0718b42
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119146283"
---
# <a name="sh_job-keyword"></a>sh \_ job-Schlüsselwort

Das **sh \_ job-Schlüsselwort** gibt an, dass `system_handle` ein ein Handle für einen Auftrag enthält.

``` syntax
[system_handle(sh_job)]

[system_handle(sh_job, access-rights)]
```

## <a name="parameters"></a>Parameter

Dieses Schlüsselwort ist ein Parameter für [**system_handle**](system-handle.md).

Die [**system_handle**](system-handle.md) dokumentation enthält auch Details zur optionalen Verwendung des *Access Rights-Parameters.* Das Standardverhalten entspricht `DUPLICATE_SAME_ACCESS` den [ **Spezifikationen der DuplicateHandle-Funktion.**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle)

## <a name="remarks"></a>Hinweise

Um dieses Schlüsselwort mit dem -Attribut verwenden zu können, muss das Flag auf (oder höher) festgelegt werden, `system_handle` `-target` wenn sie `NT100` midl.exe.

## <a name="examples"></a>Beispiele

``` syntax
interface MyInterface : IUnknown                         
{         
    HRESULT SetJob([in, system_handle(sh_job)] HANDLE job);

    HRESULT GetJobForAccounting([out, system_handle(sh_job, JOB_OBJECT_QUERY)] HANDLE* pJob);
}
```

## <a name="requirements"></a>Anforderungen

| &nbsp; | &nbsp; |
|-|-|
| Unterstützte Mindestversion (Client) | Windows 10 Anniversary Update (Version 1607, Build 14393) |
| Unterstützte Mindestversion (Server) | Windows Server 2016 (Build 14393) |

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**system_handle**](system-handle.md)
</dt> <dt>

[Auftragsobjekte](../procthread/job-objects.md)
</dt> <dt>

[Sicherheit und Zugriffsrechte für Auftragsobjekt](../procthread/job-object-security-and-access-rights.md)
</dt> <dt>

[**CreateJobObject-Funktion**](/windows/win32/api/winbase/nf-winbase-createjobobjecta)
</dt> </dl>
