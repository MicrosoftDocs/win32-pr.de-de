---
description: Die Start-Methode startet eine Aufzeichnung.
ms.assetid: 92b25afc-d5d8-47e4-a155-4ed2a3571038
title: 'Idelta-DC:: Start-Methode (Netmon. h)'
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
ms.openlocfilehash: a912af44dddb8a25d3279a5cdd7f021646c26e5d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346684"
---
# <a name="idelaydcstart-method"></a>Idelta aydc:: Start-Methode

Die **Start** -Methode startet eine Aufzeichnung.

## <a name="syntax"></a>Syntax


```C++
HRESULT STDMETHODCALLTYPE Start(
  [out] char *pFileName
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pfilename* \[ vorgenommen\]
</dt> <dd>

Zeiger auf den Namen der [*Erfassungs Datei*](c.md) , in der die Netzwerkdaten gespeichert werden. Stellen Sie sicher, dass der Dateiname zwischengespeichert wird, wenn er für den zukünftigen Verweis benötigt wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ist, ist der Rückgabewert nmerr \_ Success.

Wenn die Methode nicht erfolgreich ist, ist der Rückgabewert einer der folgenden Fehlercodes:



| Rückgabecode                                                                                           | Beschreibung                                                                                                                                                                                                                |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**nmerr- \_ Erfassung \_ angehalten**</dt> </dl> | Die Erfassung befindet sich im angehaltenen Zustand und muss beendet werden, bevor Sie neu gestartet werden kann. Nennen Sie [**idelta aydc:: Beendigung**](idelaydc-stop.md) , um die Erfassung anzuhalten. Weitere Informationen finden Sie im Abschnitt "Hinweise" in diesem Thema.<br/> |
| <dl> <dt>**nmerr- \_ Erfassung**</dt> </dl>       | Die Erfassung wurde bereits gestartet.<br/>                                                                                                                                                                                 |
| <dl> <dt>**nmerr \_ nicht \_ verbunden**</dt> </dl>  | Der npp ist nicht mit dem Netzwerk verbunden. Wenden Sie [**idelta-DC:: Connect**](idelaydc-connect.md) an, um eine Verbindung mit dem Netzwerk herzustellen.<br/>                                                                                          |
| <dl> <dt>**nmerr \_ nicht \_ verzögert**</dt> </dl>    | Der npp ist mit dem Netzwerk verbunden, jedoch nicht mit der [**idelta aydc:: Connect**](idelaydc-connect.md) -Methode.<br/>                                                                                                      |



 

## <a name="remarks"></a>Bemerkungen

Der Speicherort der [*Erfassungs Datei*](c.md) wird in der Windows-Registrierung angegeben, aber Sie können Netzwerkmonitor verwenden, um den Speicherort der Datei zu ändern.

Zum Neustarten der Erfassung mithilfe von **idelta aydc:: Start** und [**idelta aydc:: stoppmüssen**](idelaydc-stop.md)Sie die [**idelta-DC:: Configure**](idelaydc-configure.md) -Methode zum Neukonfigurieren der Verbindung bei jedem Aufruf der **idelta aydc:: Start** -Methode zum Neustarten der Datenerfassung verwenden. Wenn Sie die Erfassung mit diesen drei Methoden starten und beenden, wird jedes Mal eine neue Erfassungs Datei erstellt, wenn die Erfassung gestartet wird.

> [!Note]  
> Sie können die Erfassung auch starten und Abbrechen, indem Sie die Methoden [**idelta aydc::P ause**](idelaydc-pause.md) und [**idelta aydc:: Resume**](idelaydc-resume.md) verwenden. Wenn Sie diese beiden Methoden verwenden, werden die erfassten Daten in derselben Erfassungs Datei gespeichert.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                                                                     |
| Header<br/>                   | <dl> <dt>Netmon. h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Idelta-DC](idelaydc.md)
</dt> <dt>

[**Idelta aydc:: Configure**](idelaydc-configure.md)
</dt> <dt>

[**Idelta aydc:: Connect**](idelaydc-connect.md)
</dt> <dt>

[**Idelta aydc::P ause**](idelaydc-pause.md)
</dt> <dt>

[**Idelta aydc:: Resume**](idelaydc-resume.md)
</dt> <dt>

[**Idelta aydc:: Beendigung**](idelaydc-stop.md)
</dt> </dl>

 

 




