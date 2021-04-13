---
title: Virtualchannelgetinstance-Einstiegspunkt
description: Wird aufgerufen, damit das Plug-in eine Instanz der iwtsplugin-Schnittstelle für alle Plug-Ins erstellt, die von der dll implementiert werden.
ms.assetid: B81BD61E-1F43-42C9-8839-30F4F4C3973C
ms.tgt_platform: multiple
keywords:
- Virtualchannelgetinstance-Einstiegspunkt Remotedesktopdienste
topic_type:
- apiref
api_name:
- VirtualChannelGetInstance
api_type:
- UserDefined
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 535ebdc8928cceb282dd62de56f8c6fbadc94e90
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391718"
---
# <a name="virtualchannelgetinstance-entry-point"></a>Virtualchannelgetinstance-Einstiegspunkt

Wird aufgerufen, damit das Plug-in eine Instanz der [**iwtsplugin**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsplugin) -Schnittstelle für alle Plug-Ins erstellt, die von der dll implementiert werden.

> [!Note]
>
> Diese Funktion wird vom Plug-in implementiert und muss nach Namen exportiert werden, damit eine Anwendung die [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und die [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion verwenden kann, um dynamisch mit der Funktion zu verknüpfen.
>
> Der Prototyp für diese Funktion ist in keiner öffentlichen Header Datei enthalten, daher müssen Sie Sie genau wie gezeigt deklarieren.

 

## <a name="syntax"></a>Syntax


```C++
HRESULT VCAPITYPE VirtualChannelGetInstance(
  _In_    REFIID refiid,
  _Inout_ ULONG  *pNumObjs,
  _Out_   VOID   **ppObjArray
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*refi-ID* \[ in\]
</dt> <dd>

Gibt den Typ der zurück zugebende Schnittstelle an. Dabei muss es sich um **IID \_ iwtsplugin** handeln.

</dd> <dt>

*pnumubjs* \[ in, out\]
</dt> <dd>

Die Adresse einer **ulong** -Variablen, die die Anzahl der abgerufenen Schnittstellen empfängt.

</dd> <dt>

*ppobjarray* \[ vorgenommen\]
</dt> <dd>

Die Adresse eines Array von Zeigern, das die Schnittstellen Zeiger empfängt. Wenn dieser Parameter **null** ist, muss die Implementierung die Anzahl der Plug-ins, die von der dll implementiert werden, im *pnumubjs* -Parameter platzieren. Dies ermöglicht es dem Aufrufer, das richtige Größen Array für *ppobjarray* zuzuordnen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn dieser Einstiegspunkt erfolgreich ist, wird **S \_ OK** zurückgegeben. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/> |



 

