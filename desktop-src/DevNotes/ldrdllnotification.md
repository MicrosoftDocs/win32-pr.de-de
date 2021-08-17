---
description: Eine Benachrichtigungsrückruffunktion, die mit der LdrRegisterDllNotification-Funktion angegeben wird.
ms.assetid: 12202797-c80c-4fa3-9cc4-dcb1a9f01551
title: LdrDllNotification-Rückruffunktion
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
ms.openlocfilehash: e1e9bea21cd4e21ca7549ce34343b42c50b293471e69576d7c1164f92a371c62
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118004105"
---
# <a name="ldrdllnotification-callback-function"></a>LdrDllNotification-Rückruffunktion

\[Diese Funktion kann ohne weitere Ankündigung geändert oder Windows entfernt werden.\]

Eine Benachrichtigungsrückruffunktion, die mit der [**LdrRegisterDllNotification-Funktion angegeben**](ldrregisterdllnotification.md) wird. Das Lader ruft diese Funktion auf, wenn eine DLL zum ersten Mal geladen wird.

**Warnung:** Es ist unsicher, ob die Benachrichtigungsrückruffunktion Funktionen in einer beliebigen DLL aufruft.

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

*NotificationReason* \[ In\]
</dt> <dd>

Der Grund, aus dem die Benachrichtigungsrückruffunktion aufgerufen wurde. Dieser Parameter kann einen der folgenden Werte annehmen.



| Wert                                                                                                                                                                                                                                                                                        | Bedeutung                                                                                                                               |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LDR_DLL_NOTIFICATION_REASON_LOADED"></span><span id="ldr_dll_notification_reason_loaded"></span><dl> <dt>**LDR \_ \_ \_ DLL-BENACHRICHTIGUNGSGRUND \_ GELADEN**</dt> <dt>1</dt> </dl>       | Die DLL wurde geladen. Der *NotificationData-Parameter* verweist auf eine **BENACHRICHTIGUNGSDATENstruktur, die von der \_ LDR-DLL \_ \_ \_ geladen** wurde. <br/>     |
| <span id="LDR_DLL_NOTIFICATION_REASON_UNLOADED"></span><span id="ldr_dll_notification_reason_unloaded"></span><dl> <dt>**LDR \_ DLL \_ NOTIFICATION \_ REASON \_ UNLOADED**</dt> <dt>2</dt> </dl> | Die DLL wurde entladen. Der *NotificationData-Parameter* verweist auf eine **LDR \_ DLL \_ UNLOADED NOTIFICATION \_ \_ DATA-Struktur.** <br/> |



 

</dd> <dt>

*NotificationData* \[ In\]
</dt> <dd>

Ein Zeiger auf eine konstante **LDR \_ DLL \_ NOTIFICATION-Union,** die Benachrichtigungsdaten enthält. Diese Union hat die folgende Definition:

``` syntax
typedef union _LDR_DLL_NOTIFICATION_DATA {
    LDR_DLL_LOADED_NOTIFICATION_DATA Loaded;
    LDR_DLL_UNLOADED_NOTIFICATION_DATA Unloaded;
} LDR_DLL_NOTIFICATION_DATA, *PLDR_DLL_NOTIFICATION_DATA;
```

Die **STRUKTUR LDR \_ DLL \_ LOADED NOTIFICATION \_ \_ DATA** hat die folgende Definition:

``` syntax
typedef struct _LDR_DLL_LOADED_NOTIFICATION_DATA {
    ULONG Flags;                    //Reserved.
    PCUNICODE_STRING FullDllName;   //The full path name of the DLL module.
    PCUNICODE_STRING BaseDllName;   //The base file name of the DLL module.
    PVOID DllBase;                  //A pointer to the base address for the DLL in memory.
    ULONG SizeOfImage;              //The size of the DLL image, in bytes.
} LDR_DLL_LOADED_NOTIFICATION_DATA, *PLDR_DLL_LOADED_NOTIFICATION_DATA;
```

Die **STRUKTUR DER \_ \_ ENTLADENEN BENACHRICHTIGUNGSDATEN der \_ LDR-DLL \_** hat die folgende Definition:

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

Ein Zeiger auf Kontextdaten für die Rückruffunktion.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Rückruffunktion gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Die Benachrichtigungsrückruffunktion wird aufgerufen, bevor die dynamische Verknüpfung erfolgt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**LdrRegisterDllNotification**](ldrregisterdllnotification.md)
</dt> <dt>

[**LdrUnregisterDllNotification**](ldrunregisterdllnotification.md)
</dt> </dl>

 

 




