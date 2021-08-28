---
description: Der Experte muss die Run-Funktion implementieren. Netzwerkmonitor die Run-Funktion auf, um den Experten in der Experten-DLL zu starten.
ms.assetid: 9ef3941b-d9e9-4acb-97ed-5f39573f2946
title: Ausführen der Rückruffunktion (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Run
api_type:
- UserDefined
api_location:
- Netmon.h
ms.openlocfilehash: e31c5c729bba133fa4c4d3e36bbc54035a274923a03a8718acf05a601192775b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120074500"
---
# <a name="run-callback-function"></a>Ausführen der Rückruffunktion

Der Experte muss die **Run-Funktion** implementieren. Netzwerkmonitor ruft die **Funktion Ausführen auf,** um den Experten in der Experten-DLL zu starten.

## <a name="syntax"></a>Syntax


```C++
BOOL WINAPI Run(
  _In_ HEXPERTKEY         hExpertKey,
  _In_ PEXPERTCONFIG      pConfig,
  _In_ PEXPERTSTARTUPINFO pExpertStartupInfo,
  _In_ DWORD              StartupFlags,
  _In_ HWND               hWndParent
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hExpertKey* \[ In\]
</dt> <dd>

Eindeutiger Bezeichner des Experten, der an alle expertenspezifischen funktionen Netzwerkmonitor wird.

> [!Note]  
> Der *hExpertKey-Bezeichner* kann einen Expertenschlüssel übergeben, der sich von dem Expertenschlüssel, den die [**Configure-Funktion übergibt,**](configure.md) unterscheiden kann.

 

</dd> <dt>

*pConfig* \[ In\]
</dt> <dd>

Zeiger auf die vorhandene Konfiguration. Der *pConfig-Parameter* kann **NULL sein,** was bedeutet, dass der Experte mit hart codierten Standardwerten oder Startinformationen ausgeführt werden kann, auf die der *Parameter pExpertStartupInfo* verweist.

</dd> <dt>

*pExpertStartupInfo* \[ In\]
</dt> <dd>

Zeiger auf das Erfassungselement, das den Fokus besitzt, wenn der Experte startet.

</dd> <dt>

*StartupFlags* \[ In\]
</dt> <dd>

Gibt an, wie der Experte den *Parameter pExpertStartupInfo verwenden* soll.

Das einzige definierte Flag ist:



| Wert                                                                                                                                                                                                                                                                                           | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                                                       |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="EXPERT_STARTUP_FLAG_USE_STARTUP_DATA_OVER_CONFIG_DATA."></span><span id="expert_startup_flag_use_startup_data_over_config_data."></span><dl> <dt>**\_STARTFLAG DES EXPERTEN VERWENDEN \_ \_ \_ \_ STARTDATEN ÜBER \_ \_ \_ KONFIGURATIONSDATEN.**</dt> </dl> | Dieses Flag gibt an, dass der Experte den *Parameter pExpertStartupInfo* und nicht den *Parameter pConfig* verwendet. In der Regel können Sie dieses Flag festlegen, wenn der Experte mit einem Rechtsklick beginnen kann. Wenn das Flag nicht festgelegt ist, können die folgenden beiden Dinge auftreten: Entweder startet der Experte nicht mit der rechten Maustaste, oder der Experte startet mit der rechten Maustaste, und der Benutzer konfiguriert es.<br/> |



 

</dd> <dt>

*hWndParent* \[ In\]
</dt> <dd>

Der *hWnd-Parameter* des übergeordneten Elements (in der Regel Netzwerkmonitor Benutzeroberfläche).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist (d. h. wenn der Experte startet), ist der Rückgabewert **TRUE.**

Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert **FALSE.**

## <a name="remarks"></a>Hinweise

Bei der Ausführung durchschleifet der Experte die Frames in der Erfassungsdatei und generiert entweder einen Bericht oder Ereignisse, die Probleme anzeigen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



 

 




