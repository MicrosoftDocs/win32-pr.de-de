---
title: enable_allocate-Attribut
description: Das Attribut \ enable \_ attributs\acf gibt an, dass der Serverstub-Code die Stub-Speicher Verwaltungs Umgebung aktivieren soll.
ms.assetid: 3a232a82-f114-4d8c-8b71-cf8860c77db3
keywords:
- enable_allocate Attribut-Mittel l
topic_type:
- apiref
api_name:
- enable_allocate
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f43e8c10592fcf99ea294327c400c579ce45bf6b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104101506"
---
# <a name="enable_allocate-attribute"></a>\_Attribut zuweisen aktivieren

Das Attribut "Zuordnungs-ACF **\[ aktivieren \_ \]** " gibt an, dass der serverstubcode die Stub-Speicher Verwaltungs Umgebung aktivieren soll.

> [!Note]  
> Das Attribut " **\[ \_ zuordnen \]** " ist veraltet und wird nicht mehr unterstützt.

 

``` syntax
[
    enable_allocate
  [ , optional-attribute-list]
]
interface interface-name
{
    . . .
};
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*optional-Attribut-List* 
</dt> <dd>

Gibt eine Liste von 0 (null) oder mehr zusätzlichen Mittelwert Attributen an.

</dd> <dt>

*Schnittstellen Name* 
</dt> <dd>

Der Name der Schnittstelle, auf die das **\[ enable \_ allcoate \]** -Attribut angewendet wird.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Im Standardmodus aktiviert der Serverstub die Arbeitsspeicher Umgebung nur, wenn das Attribut " **\[ \_ zuordnen \]** " verwendet wird. Die Speicher Verwaltungs Umgebung muss aktiviert werden, damit der Arbeitsspeicher mithilfe von [**rpcsmallozugewiesen**](/windows/desktop/api/rpcndr/nf-rpcndr-rpcsmallocate)werden kann. Im **eines Zertifikats** -Modus (bei der Kompilierung mithilfe des [**/OSF**](-osf.md) -Schalters) aktiviert der Stub diese Umgebung automatisch oder bei einer Anforderung, wenn das Attribut " **\[ \_ zuordnen \]** " verwendet wird.

Der Client seitige Stub kann für die **RPCSS** -Speicher Verwaltungs Umgebung empfindlich sein. Wenn ein sensibler Clientstub ausgeführt wird, wenn das **RPCSS** -Paket deaktiviert ist, werden die standardmäßigen benutzerallokator/-deallocators aufgerufen (z. b. " [Mittel l Benutzer", wenn Sie den \_ \_](/windows/desktop/Rpc/the-midl-user-allocate-function) /  [ \_ Benutzer \_ kostenlos](/windows/desktop/Rpc/the-midl-user-free-function)zuweisen). Wenn diese Option aktiviert ist, verwendet das **RPCSS** -Paket das zuordnerpaar/das dezuordnerpaar aus dem Paket. Im Standardmodus ist der Client nur dann sensibel, wenn das Attribut " **\[ \_ zuordnen \]** " verwendet wird. In der Regel arbeitet der Client seitige Stub in der deaktivierten Umgebung. Im **eines Zertifikats** -Modus (bei der Kompilierung mithilfe des [**/OSF**](-osf.md) -Schalters) ist der Client immer für die **RPCSS** -Speicher Verwaltungs Umgebung sensibel. Daher wirkt sich das Attribut " **\[ \_ zuordnen \]** " nicht auf die Clientstub aus.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Anwendungs Konfigurationsdatei (ACF)](application-configuration-file-acf-.md)
</dt> <dt>

[mittlere Benutzer Zuordnungen \_ \_](/windows/desktop/Rpc/the-midl-user-allocate-function)
</dt> <dt>

[mittlerer l- \_ Benutzer \_ kostenlos](/windows/desktop/Rpc/the-midl-user-free-function)
</dt> <dt>

[**/osf**](-osf.md)
</dt> <dt>

[Rpcsmdisablezuordnen](/windows/desktop/api/rpcndr/nf-rpcndr-rpcsmdisableallocate)
</dt> <dt>

[Rpcsmenablezuordnen](/windows/desktop/api/rpcndr/nf-rpcndr-rpcsmenableallocate)
</dt> <dt>

[Rpcsmfree](/windows/desktop/api/rpcndr/nf-rpcndr-rpcsmfree)
</dt> </dl>

 

 