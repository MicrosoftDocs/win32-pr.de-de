---
description: Eine abstrakte Basisklasse, von der alle Datenklassen des Machine Check Architecture(MCA)-Anbieters abgeleitet werden, z. B. MSMCAInfo \_ RawMCAData. Diese Klasse ist nur in 64-Bit-Systemen Windows verfügbar.
ms.assetid: 22ec8343-fc4f-4b14-9354-26b5d6a6fe09
title: MSMCAInfo-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAInfo
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: cef9878ea8e9dd6c11c6b18a62d332e17f24810548360e0edb9c117e02a710c4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119051188"
---
# <a name="msmcainfo-class"></a>MSMCAInfo-Klasse

Die **MSMCAInfo-Klasse** ist eine abstrakte Basisklasse, von der alle Datenklassen des Machine Check Architecture-Anbieters (Machine Check Architecture, MCA), z. B. [**MSMCAInfo \_ RawMCAData,**](msmcainfo-rawmcadata.md)abgeleitet werden. Der MCA-Anbieter verfügt auch über Ereignisklassen, die von [**WMIEvent abgeleitet sind.**](wmievent.md) Diese Klasse ist nur in 64-Bit-Systemen Windows verfügbar.

Die folgende Syntax wird durch Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften. Eigenschaften und Methoden sind in alphabetischer Reihenfolge und nicht in MOF-Reihenfolge.

## <a name="syntax"></a>Syntax

``` syntax
class MSMCAInfo
{
};
```

## <a name="members"></a>Member

Die **MSMCAInfo-Klasse** definiert keine Member.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows XP<br/>                                                                  |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2003<br/>                                                         |
| Namespace<br/>                | Root \\ wmi<br/>                                                                   |
| MOF<br/>                      | <dl> <dt>Wmicore.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wmiprov.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[MSMCA-Klassen](msmca-classes.md)
</dt> <dt>

[**MSMCAEvent-Header \_**](msmcaevent-header.md)
</dt> <dt>

[**WMIEvent**](wmievent.md)
</dt> </dl>

 

 




