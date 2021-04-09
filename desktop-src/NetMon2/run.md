---
description: Der Experte muss die Run-Funktion implementieren. Netzwerkmonitor Ruft die Run-Funktion auf, um den Experten innerhalb der Experten-dll zu starten.
ms.assetid: 9ef3941b-d9e9-4acb-97ed-5f39573f2946
title: Run Callback-Funktion (Netmon. h)
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
ms.openlocfilehash: c2dff2cf70a6d989928f17447fa3491dd9509f24
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862899"
---
# <a name="run-callback-function"></a>Rückruffunktion ausführen

Der Experte muss die **Run** -Funktion implementieren. Netzwerkmonitor Ruft die **Run** -Funktion auf, um den Experten innerhalb der Experten-dll zu starten.

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

*hexpertkey* \[ in\]
</dt> <dd>

Eindeutiger Bezeichner des Experten, der an alle expertenspezifischen Netzwerkmonitor Funktionen zurückgegeben wird.

> [!Note]  
> Der *hexpertkey* -Bezeichner kann einen anderen als den von der Funktion " [**configure**](configure.md) " übergebenen expertenschlüssel übergeben.

 

</dd> <dt>

*pConfig* \[ in\]
</dt> <dd>

Zeiger auf die vorhandene Konfiguration. Der *pConfig* -Parameter kann **null** sein, was bedeutet, dass der Experte mit hart codierten Standardwerten oder Startinformationen, auf die der *pexpertstartupinfo* -Parameter verweist, ausgeführt werden kann.

</dd> <dt>

*pexpertstartupinfo* \[ in\]
</dt> <dd>

Zeiger auf das Erfassungs Element, das den Fokus besitzt, wenn der Experte gestartet wird.

</dd> <dt>

*StartupFlags* \[ in\]
</dt> <dd>

Indikator dafür, wie der Experte den *pexpertstartupinfo* -Parameter verwenden soll.

Das einzige Flag, das definiert ist, ist:



| Wert                                                                                                                                                                                                                                                                                           | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                                                       |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="EXPERT_STARTUP_FLAG_USE_STARTUP_DATA_OVER_CONFIG_DATA."></span><span id="expert_startup_flag_use_startup_data_over_config_data."></span><dl> <dt>**Das \_ \_ Startflag für Experten \_ verwendet \_ Start \_ Daten für \_ \_ Konfigurations \_ Daten.**</dt> </dl> | Dieses Flag gibt an, dass der Experte den *pexpertstartupinfo* -Parameter verwendet und nicht den *pConfig* -Parameter verwendet. In der Regel können Sie dieses Flag festlegen, wenn der Experte von einem Rechtsklick aus beginnen kann. Wenn das Flag nicht festgelegt ist, können die folgenden beiden Aktionen auftreten: entweder der Experte startet nicht mit der rechten Maustaste, oder der Experte startet mit der rechten Maustaste, und der Benutzer konfiguriert ihn.<br/> |



 

</dd> <dt>

*hwndParent* \[ in\]
</dt> <dd>

Der *HWND* -Parameter des übergeordneten Elements (normalerweise die Netzwerkmonitor Benutzeroberfläche).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist (d. h., wenn der Experte startet), ist der Rückgabewert " **true**".

Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert **false**.

## <a name="remarks"></a>Bemerkungen

Beim Ausführen durchläuft der Experte die Frames in der Erfassungs Datei und generiert entweder einen Bericht oder erstellt Ereignisse, die Probleme anzeigen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




