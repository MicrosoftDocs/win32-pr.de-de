---
description: Lädt die Monitor-DLL.
ms.assetid: 6de2750f-3f12-4c0a-af8d-3ebd227fa123
title: Onloadingdll-Funktion (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OnLoadingDLL
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: b2d9d728065818b1e94fa436f4d1e9b62dbeb5cd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106357394"
---
# <a name="onloadingdll-function"></a>Onloadingdll-Funktion

Die **onloadingdll** -Funktion lädt die Monitor-DLL.

## <a name="syntax"></a>Syntax


```C++
HRESULT OnLoadingDLL(
  _Inout_ HBLOB hFilterBlob,
  _In_    DWORD *pCreateFlags,
  _Out_   char  **ppDefaultName,
  _Out_   char  **ppDescription,
  _Out_   char  **ppDefaultScript,
  _Out_   char  **ppDefaultConfig
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hfilterblob* \[ in, out\]
</dt> <dd>

Ein BLOB, das von mcsvc verwendet wird, um einen Monitor mit verfügbaren NICs abzugleichen. Dieser Parameter enthält immer eine Anforderung für eine [untc](irtc.md) -Schnittstelle, sodass die meisten Monitore dem BLOB keine Einträge hinzufügen müssen. Ein benutzerdefinierter Monitor kann jedoch zusätzliche Filterkriterien hinzufügen (z. b., dass der Mac-Typ Ethernet lauten muss).

</dd> <dt>

*pkreateflags* \[ in\]
</dt> <dd>

Die Flags, die angeben, wie mcsvc die Erstellung eines Monitors steuert. Dieser Parameter muss einen der folgenden Werte aufweisen:



| Wert                                                                                                                                                                                                            | Bedeutung                                                                                                                                                       |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MCS_CREATE_ONE_PER_NETCARD"></span><span id="mcs_create_one_per_netcard"></span><dl> <dt>**MCS \_ Create \_ One \_ per \_ Netcard**</dt> </dl>          | Mcsvc stellt sicher, dass nur eine Instanz dieses Monitors für jede NIC vorhanden ist. Eine zweite Instanz kann nur erstellt werden, wenn die erste Instanz zerstört wird.<br/> |
| <span id="MCS_CREATE_CONFIGS_BY_DEFAULT"></span><span id="mcs_create_configs_by_default"></span><dl> <dt>**MCS \_ Erstellen \_ von Konfigurationen \_ \_ standardmäßig**</dt> </dl> | Wenn der Monitor über eine interne Standardkonfiguration verfügt, muss der Benutzer von mcsvc nicht konfiguriert werden, bevor die Instanz erstellt wird.<br/>  |



 

</dd> <dt>

*ppdefaultname* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf einen Zeiger auf die Adresse des Standard namens des Monitors. Der mcsvc verwendet beim Erstellen von Instanzen des Monitors den Standardnamen.

Wenn der zurückgegebene Standardname beispielsweise "Router Monitor" lautet, ist die erste Monitor Instanz "Router Monitor 1", die zweite "RouterMonitor2" usw. Wenn **null** zurückgegeben wird, verwendet mcsvc den Namen der dll.

</dd> <dt>

*ppdescription* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf einen Zeiger auf die Adresse der Beschreibung des Monitors. Die Beschreibung wird an das Monitor-Steuerungs Tool übermittelt, das die Beschreibung verwendet, um dem Benutzer mitzuteilen, dass der Monitor vorhanden ist. Dieser Parameter kann **null** zurückgeben.

</dd> <dt>

*ppdefaultscript* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf einen Zeiger auf die Adresse des standardmäßigen HTML-Formular Skripts, das zum Konfigurieren des Monitors verwendet wird. Obwohl die Instanzen des Monitors Ihr eigenes Skript ändern können, laden die meisten Monitore das Skript einfach einmal aus einer Datei. Der Wert von *ppdefaultscript* kann **null** sein. der Monitor kann jedoch nicht extern konfiguriert werden, oder er muss später ein Skript bereitstellen. Es ist effizienter, hier ein Standardskript bereitzustellen.

</dd> <dt>

*ppdefaultconfig* \[ vorgenommen\]
</dt> <dd>

Die Adresse der Standard Zeichenfolge, die verwendet wird, um den Monitor zu konfigurieren, wenn er erstellt wird. Dieser Parameter kann auf **null** festgelegt werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, ist der Rückgabewert S \_ OK. Dies entspricht noError.

Wenn die Funktion nicht erfolgreich ist, wird der angegebene Monitor von der mcsvc aus allen Listen ausgelassen. nach kann kein Monitor dieses Typs erstellt werden.

## <a name="remarks"></a>Bemerkungen

Die **onloadingdll** -Funktion wird von mcsvc einmal aufgerufen, wenn die dll zum ersten Mal geladen wird. Die dll stellt dann die Standardwerte bereit, die von mcsvc beim Erstellen einer Instanz eines Monitors verwendet werden.

Der Monitor muss den gesamten erforderlichen Arbeitsspeicher für die Zeichen folgen zuordnen, die an mcsvc zurückgegeben werden. Bei der Rückgabe werden von mcsvc Kopien aller Zeichen folgen erstellt, und es wird nicht versucht, die zurückgegebenen Zeichen folgen freizugeben.

Der Monitor sollte BLOB-Hilfsobjekte verwenden, um das filterblob zu ändern.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




