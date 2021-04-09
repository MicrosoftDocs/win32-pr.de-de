---
description: Eine Benachrichtigungs Rückruffunktion, die mit der ldrregisterdllnotification-Funktion angegeben wird.
ms.assetid: 12202797-c80c-4fa3-9cc4-dcb1a9f01551
title: Ldrdllnotification-Rückruffunktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LdrDllNotification
- PLDR_DLL_NOTIFICATION_FUNCTION
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: e29cd7b17c634250f56cbafcf86379449ac88199
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103860603"
---
# <a name="ldrdllnotification-callback-function"></a>Ldrdllnotification-Rückruffunktion

\[Diese Funktion kann ohne vorherige Ankündigung geändert oder aus Windows entfernt werden.\]

Eine Benachrichtigungs Rückruffunktion, die mit der [**ldrregisterdllnotification**](ldrregisterdllnotification.md) -Funktion angegeben wird. Das Lade Modul ruft diese Funktion auf, wenn eine DLL zum ersten Mal geladen wird.

**Warnung:** Es ist unsicher, dass die Benachrichtigungs Rückruffunktion Funktionen in einer beliebigen DLL aufruft.

## <a name="syntax"></a>Syntax


```C++
VOID CALLBACK LdrDllNotification(
  _In_     ULONG                       NotificationReason,
  _In_     PCLDR_DLL_NOTIFICATION_DATA NotificationData,
  _In_opt_ PVOID                       Context
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Notificationreason* \[ in\]
</dt> <dd>

Der Grund, warum die Benachrichtigungs Rückruffunktion aufgerufen wurde. Dieser Parameter kann einen der folgenden Werte annehmen.



| Wert                                                                                                                                                                                                                                                                                        | Bedeutung                                                                                                                               |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LDR_DLL_NOTIFICATION_REASON_LOADED"></span><span id="ldr_dll_notification_reason_loaded"></span><dl> <dt>**LDR \_ DLL- \_ Benachrichtigungs \_ Grund \_ geladen**</dt> <dt>1</dt> </dl>       | Die dll wurde geladen. Der *notificationdata* -Parameter verweist auf eine von der **LDR- \_ dll \_ geladene \_ Benachrichtigungs \_ Daten** Struktur. <br/>     |
| <span id="LDR_DLL_NOTIFICATION_REASON_UNLOADED"></span><span id="ldr_dll_notification_reason_unloaded"></span><dl> <dt>**LDR \_ DLL- \_ Benachrichtigungs \_ Grund \_ entladen**</dt> <dt>2</dt> </dl> | Die dll wurde entladen. Der *notificationdata* -Parameter verweist auf eine von der **LDR- \_ dll \_ entladene \_ Benachrichtigungs \_ Daten** Struktur. <br/> |



 

</dd> <dt>

*Notificationdata* \[ in\]
</dt> <dd>

Ein Zeiger auf eine Konstante **LDR- \_ dll- \_ Benachrichtigungs** Union, die Benachrichtigungs Daten enthält. Diese Union weist die folgende Definition auf:

``` syntax
typedef union _LDR_DLL_NOTIFICATION_DATA {
    LDR_DLL_LOADED_NOTIFICATION_DATA Loaded;
    LDR_DLL_UNLOADED_NOTIFICATION_DATA Unloaded;
} LDR_DLL_NOTIFICATION_DATA, *PLDR_DLL_NOTIFICATION_DATA;
```

Die von der **LDR- \_ dll \_ geladene \_ Benachrichtigungs \_ Daten** Struktur weist die folgende Definition auf:

``` syntax
typedef struct _LDR_DLL_LOADED_NOTIFICATION_DATA {
    ULONG Flags;                    //Reserved.
    PCUNICODE_STRING FullDllName;   //The full path name of the DLL module.
    PCUNICODE_STRING BaseDllName;   //The base file name of the DLL module.
    PVOID DllBase;                  //A pointer to the base address for the DLL in memory.
    ULONG SizeOfImage;              //The size of the DLL image, in bytes.
} LDR_DLL_LOADED_NOTIFICATION_DATA, *PLDR_DLL_LOADED_NOTIFICATION_DATA;
```

Die **\_ \_ ungeladene \_ Benachrichtigungs \_ Datenstruktur der LDR-dll** weist die folgende Definition auf:

``` syntax
typedef struct _LDR_DLL_UNLOADED_NOTIFICATION_DATA {
    ULONG Flags;                    //Reserved.
    PCUNICODE_STRING FullDllName;   //The full path name of the DLL module.
    PCUNICODE_STRING BaseDllName;   //The base file name of the DLL module.
    PVOID DllBase;                  //A pointer to the base address for the DLL in memory.
    ULONG SizeOfImage;              //The size of the DLL image, in bytes.
} LDR_DLL_UNLOADED_NOTIFICATION_DATA, *PLDR_DLL_UNLOADED_NOTIFICATION_DATA;
```

</dd> <dt>

*Kontext* \[ in, optional\]
</dt> <dd>

Ein Zeiger auf die Kontext Daten für die Rückruffunktion.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Rückruffunktion gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Die Benachrichtigungs Rückruffunktion wird aufgerufen, bevor dynamische Verknüpfungen stattfinden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ldrregisterdllnotification**](ldrregisterdllnotification.md)
</dt> <dt>

[**Ldrunregisterdllnotification**](ldrunregisterdllnotification.md)
</dt> </dl>

 

 




