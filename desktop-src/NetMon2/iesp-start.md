---
description: 'IESP::Start-Methode: Die Start-Methode startet eine Erfassung.'
ms.assetid: 8bf8c0c7-20be-4404-8ea5-b28b4c658523
title: IESP::Start-Methode (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IESP.Start
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 8023b9db00834b10fcce84510df5ccbafec0c7a2f6654ef73d71754e7c563044
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118365580"
---
# <a name="iespstart-method"></a>IESP::Start-Methode

Die **Start-Methode** startet eine Erfassung.

## <a name="syntax"></a>Syntax


```C++
HRESULT STDMETHODCALLTYPE Start(
  [out] char *pFileName
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pFileName* \[ out\]
</dt> <dd>

Zeiger auf den Namen der [*Erfassungsdatei,*](c.md) die zum Speichern der Netzwerkdaten verwendet wird. Stellen Sie sicher, dass Sie diesen Dateinamen zwischenspeichern, wenn er für zukünftige Verweise benötigt wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ist, lautet der Rückgabewert NMERR \_ SUCCESS.

Wenn die Methode nicht erfolgreich ist, ist der Rückgabewert einer der folgenden Fehlercodes:



| Rückgabecode                                                                                           | Beschreibung                                                                                                                            |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NMERR \_ CAPTURE \_ PAUSED**</dt> </dl> | Die Erfassung wird angehalten und muss beendet werden, bevor sie neu gestartet werden kann. Rufen Sie [IESP::Stop](iesp-stop.md) auf, um die Erfassung zu beenden.<br/> |
| <dl> <dt>**\_NMERR-ERFASSUNG**</dt> </dl>       | Die Erfassung wurde bereits gestartet.<br/>                                                                                             |
| <dl> <dt>**NMERR \_ NICHT \_ VERBUNDEN**</dt> </dl>  | Das NPP ist nicht mit dem Netzwerk verbunden. Rufen Sie [IESP::Verbinden](iesp-connect.md) auf, um das NPP mit dem Netzwerk zu verbinden.<br/>          |
| <dl> <dt>**NMERR \_ NOT \_ ESP**</dt> </dl>        | Das NPP ist mit dem Netzwerk verbunden, jedoch nicht mit der [IESP::Verbinden-Methode.](iesp-connect.md)<br/>                              |



 

## <a name="remarks"></a>Hinweise

Der Speicherort der [*Erfassungsdatei*](c.md) wird in der Windows-Registrierung angegeben. Sie können jedoch Netzwerkmonitor verwenden, um den Verzeichnisspeicherort zu ändern.

Wenn Sie die Erfassung mithilfe der Methoden IESP::Start und [IESP::Stop](iesp-stop.md) neu starten, müssen Sie die [IESP::Configure-Methode](iesp-configure.md) aufrufen, um die Verbindung jedes Mal neu zu konfigurieren, wenn Sie IESP::Start aufrufen, um die Erfassungsdaten neu zu starten. Wenn Sie die Erfassung mit diesen drei Methoden starten und beenden, wird bei jedem Start der Erfassung eine neue Erfassungsdatei erstellt.

> [!Note]  
> Sie können die Erfassung auch mithilfe der [Methoden IESP::P ause](iesp-pause.md) und [IESP::Resume](iesp-resume.md) starten und beenden. Wenn diese beiden Methoden verwendet werden, werden die erfassten Daten in derselben Erfassungsdatei gespeichert.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                                                                     |
| Header<br/>                   | <dl> <dt>Netmon.h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[IESP](iesp.md)
</dt> <dt>

[IESP::Configure](iesp-configure.md)
</dt> <dt>

[IESP::Verbinden](iesp-connect.md)
</dt> <dt>

[IESP::P ause](iesp-pause.md)
</dt> <dt>

[IESP::Resume](iesp-resume.md)
</dt> <dt>

[IESP::Stop](iesp-stop.md)
</dt> </dl>

 

 




