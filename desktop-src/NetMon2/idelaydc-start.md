---
description: 'IDelaydC::Start-Methode: Die Start-Methode startet eine Erfassung.'
ms.assetid: 92b25afc-d5d8-47e4-a155-4ed2a3571038
title: IDelaydC::Start-Methode (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDelaydC.Start
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 750a33241358aee924ed3f91491185117a77a548a87bdfc5514d59fe4798a42c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118365865"
---
# <a name="idelaydcstart-method"></a>IDelaydC::Start-Methode

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

Wenn die Methode erfolgreich ist, ist der Rückgabewert NMERR \_ SUCCESS.

Wenn die Methode nicht erfolgreich ist, ist der Rückgabewert einer der folgenden Fehlercodes:



| Rückgabecode                                                                                           | Beschreibung                                                                                                                                                                                                                |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NMERR \_ CAPTURE \_ PAUSED**</dt> </dl> | Die Erfassung befindet sich in einem angehaltenen Zustand und muss beendet werden, bevor sie neu gestartet werden kann. Rufen [**Sie IDelaydC::Stop auf,**](idelaydc-stop.md) um die Erfassung zu beenden. Weitere Informationen finden Sie im Abschnitt "Hinweise" in diesem Thema.<br/> |
| <dl> <dt>**NMERR-ERFASSUNG \_**</dt> </dl>       | Die Erfassung wurde bereits gestartet.<br/>                                                                                                                                                                                 |
| <dl> <dt>**NMERR \_ NICHT \_ VERBUNDEN**</dt> </dl>  | Der NPP ist nicht mit dem Netzwerk verbunden. Rufen [**Sie IDelaydC::Verbinden**](idelaydc-connect.md) auf, um eine Verbindung mit dem Netzwerk herzustellen.<br/>                                                                                          |
| <dl> <dt>**NMERR \_ NICHT \_ VERZÖGERT**</dt> </dl>    | Das NPP ist mit dem Netzwerk verbunden, aber nicht mit der [**IDelaydC::Verbinden-Methode.**](idelaydc-connect.md)<br/>                                                                                                      |



 

## <a name="remarks"></a>Hinweise

Der Speicherort der [*Erfassungsdatei*](c.md) wird in Ihrer Windows-Registrierung angegeben, aber Sie können Netzwerkmonitor verwenden, um den Speicherort der Datei zu ändern.

Um die Erfassung **mithilfe von IDelaydC::Start und** [**IDelaydC::Stop**](idelaydc-stop.md)neu zu starten, müssen Sie die [**IDelaydC::Configure-Methode**](idelaydc-configure.md) aufrufen, um die Verbindung jedes Mal neu zu konfigurieren, wenn Sie die **IDelaydC::Start-Methode** aufrufen, um die Erfassung von Daten neu zu starten. Wenn Sie die Erfassung mit diesen drei Methoden starten und beenden, wird bei jedem Start der Erfassung eine neue Erfassungsdatei erstellt.

> [!Note]  
> Sie können die Erfassung auch mithilfe der [**Methoden IDelaydC::P ause und**](idelaydc-pause.md) [**IDelaydC::Resume**](idelaydc-resume.md) starten und beenden. Wenn Sie diese beiden Methoden verwenden, werden die erfassten Daten in derselben Erfassungsdatei gespeichert.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                                                                     |
| Header<br/>                   | <dl> <dt>Netmon.h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[IDelaydC](idelaydc.md)
</dt> <dt>

[**IDelaydC::Configure**](idelaydc-configure.md)
</dt> <dt>

[**IDelaydC::Verbinden**](idelaydc-connect.md)
</dt> <dt>

[**IDelaydC::P ause**](idelaydc-pause.md)
</dt> <dt>

[**IDelaydC::Resume**](idelaydc-resume.md)
</dt> <dt>

[**IDelaydC::Stop**](idelaydc-stop.md)
</dt> </dl>

 

 




