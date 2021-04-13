---
UID: ''
title: Lsamanagesidnamemapping-Funktion
description: Fügt sid/Name-Zuordnungen aus dem im LSA-lookupdienst registrierten Zuordnungs Satz hinzu oder entfernt Sie.
old-location: ''
ms.assetid: na
ms.date: 04/10/2019
ms.keywords: ''
ms.topic: reference
req.header: Ntsecapi.h
req.include-header: ''
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: Secur32.lib
req.dll:
- Advapi32.dll
- API-MS-Win-DownLevel-AdvAPI32-l4-1-0.dll
- API-MS-Win-security-lsalookup-l2-1-1.dll
req.irql: ''
topic_type:
- APIRef
api_type: ''
api_location: ''
api_name:
- LsaManageSidNameMapping
targetos: Windows
req.typenames: ''
req.redist: ''
ms.openlocfilehash: fc0065c3964718d690149693f3c71ec4e9f676ec
ms.sourcegitcommit: 382c7259008374408368c173e0027fb641c848fe
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/22/2020
ms.locfileid: "104314494"
---
# <a name="lsamanagesidnamemapping-function"></a>Lsamanagesidnamemapping-Funktion

## <a name="description"></a>BESCHREIBUNG

Die **lsamanagesidnamemapping** -Funktion fügt sid/Name-Zuordnungen aus dem mit dem LSA-lookupdienst registrierten Zuordnungs Satz hinzu oder entfernt Sie.

```cpp
void WINAPI LsaManageSidNameMapping(
  _In_  LSA_SID_NAME_MAPPING_OPERATION_TYPE    OpType,
  _In_  PLSA_SID_NAME_MAPPING_OPERATION_INPUT  OpInput,
  _Out_ PLSA_SID_NAME_MAPPING_OPERATION_OUTPUT *OpOutput
);
```

## <a name="parameters"></a>Parameter

### <a name="optype-in"></a>Optype [in]

Gibt an, ob diese Funktion aufgerufen wird, um eine SID/Name-Zuordnung hinzuzufügen oder zu entfernen.

### <a name="opinput-in"></a>Opinput [in]

Gibt die Domänen-, Konto-und sid-Werte an, die während dieses Vorgangs verwendet werden sollen. Zusätzliche Flags können auch in dieser Struktur festgelegt werden.

### <a name="opoutput-out"></a>Opoutput [out]

Enthält den Wert [LSA_SID_NAME_MAPPING_OPERATION_ERROR](/previous-versions/windows/desktop/legacy/dn280707(v=vs.85)) , der einen erfolgreichen oder fehlgeschlagener Vorgang angibt.

| Wert | Bedeutung |
|-------|---------|
| **Erfolgreich** | Der Vorgang ist ohne Fehler beendet. |
| **Nonmappingerror** | Ein Fehler, der nicht mit der SID-Namenszuordnung verknüpft ist. |
| **Namecollision** | Vorgangs Fehler aufgrund eines Namens Konflikts. |
| **Sidcollision** | Vorgangs Fehler aufgrund eines sid-Konflikts. |
| **DomainNotFound** | Die zugehörige Domäne wurde nicht gefunden. |
| **Domainsidprefixmismatch** | Die angegebene sid weist nicht das richtige Domänen Präfix auf. |
| **Mappingnotfound** | Die Zuordnung wurde im Cache nicht gefunden. |

## <a name="returns"></a>Gibt zurück

Wenn die Zuordnung erfolgreich eingefügt wird, wird der Rückgabewert STATUS_SUCCESS.
Wenn die Funktion andernfalls aufgrund von sid-oder Namenskonflikten fehlschlägt, wird STATUS_INVALID_PARAMETER Fehler zurückgegeben.

## <a name="remarks"></a>Bemerkungen

## <a name="see-also"></a>Siehe auch
