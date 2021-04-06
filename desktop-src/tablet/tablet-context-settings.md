---
description: Enthält Informationen, die zum Erstellen eines Tablet-Kontexts verwendet werden.
ms.assetid: 10466c23-f4cb-4205-886b-d85a2f530afe
title: TABLET_CONTEXT_SETTINGS Struktur
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TABLET_CONTEXT_SETTINGS
api_type:
- NA
api_location: ''
ms.openlocfilehash: 9357281409ed4c48b4c6013a7a2be2997d58b094
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960855"
---
# <a name="tablet_context_settings-structure"></a>Struktur der Tablet- \_ Kontext \_ Einstellungen

Enthält Informationen, die zum Erstellen eines Tablet-Kontexts verwendet werden.

## <a name="syntax"></a>Syntax


```C++
typedef struct _TABLET_CONTEXT_SETTINGS {
  ULONG cPktProps;
  GUID  *pguidPktProps;
  ULONG cPktBtns;
  GUID  *pguidPktBtns;
  DWORD *pdwBtnDnMask;
  DWORD *pdwBtnUpMask;
  LONG  lXMargin;
  LONG  lYMargin;
} TABLET_CONTEXT_SETTINGS;
```



## <a name="members"></a>Member

<dl> <dt>

**cpkt-Eigenschaften**
</dt> <dd>

Die Anzahl der Eigenschaften in einem Paket.

</dd> <dt>

**pguidpkt-Eigenschaften**
</dt> <dd>

Eindeutige Bezeichner für die Paket Eigenschaften.

</dd> <dt>

**cpktbtns**
</dt> <dd>

Die Anzahl der Schaltflächen.

</dd> <dt>

**pguidpktbtns**
</dt> <dd>

Eindeutige Bezeichner für die Schaltflächen.

</dd> <dt>

**pdwbtndnmask**
</dt> <dd>

Die Schaltflächen-ab-Maske.

</dd> <dt>

**pdwbtnupmask**
</dt> <dd>

Die Schaltfläche "nach oben".

</dd> <dt>

**lxmargin**
</dt> <dd>

Der X-Richtung Rand.

</dd> <dt>

**lymargin**
</dt> <dd>

Der Y-Richtung Rand.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

In der Regel Ruft eine Anwendung die Standardwerte aus der [**iTablet:: getdefaultcontextsettings-Methode**](itablet-getdefaultcontextsettings.md)ab, ändert die Werte entsprechend Ihren Anforderungen und übergibt dann die geänderte Einstellungs Struktur an die [**iTablet:: deecontext-Methode**](itablet-createcontext.md).

Diese Struktur bestimmt, welche Ereignisse eine Anwendung erhält, wie Sie verarbeitet werden und wie Sie an die Anwendung oder an Windows selbst übermittelt werden.

Die Schaltflächen Masken legen fest, welche Arten von Ereignissen vom Kontext verarbeitet werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                     |



 

 




