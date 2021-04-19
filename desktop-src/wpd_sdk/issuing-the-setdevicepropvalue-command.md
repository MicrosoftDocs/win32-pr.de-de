---
description: Ausgeben des Befehls "setdevicepropvalue"
ms.assetid: d5917421-fbd4-477c-b29b-9f983c93cfdb
title: Ausgeben des Befehls "setdevicepropvalue"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8949cbf4fe22662de32c4c07de689fec2e6dbad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349697"
---
# <a name="issuing-the-setdevicepropvalue-command"></a><span data-ttu-id="2cdad-103">Ausgeben des Befehls "setdevicepropvalue"</span><span class="sxs-lookup"><span data-stu-id="2cdad-103">Issuing the SetDevicePropValue Command</span></span>

<span data-ttu-id="2cdad-104">Im Beispiel in diesem Abschnitt wird der Befehl **setdevicepropvalue** MTP aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="2cdad-104">The example in this section invokes the **SetDevicePropValue** MTP command.</span></span> <span data-ttu-id="2cdad-105">(Eine ausführliche Beschreibung dieses Befehls und seiner Parameter finden Sie in der [MTP-Spezifikation](https://www.usb.org/sites/default/files/MTPv1_1.zip).)</span><span class="sxs-lookup"><span data-stu-id="2cdad-105">(For a complete description of this command and its parameters, see the [MTP specification](https://www.usb.org/sites/default/files/MTPv1_1.zip).)</span></span>

<span data-ttu-id="2cdad-106">Da dieser Befehl Daten (oder eine Daten Phase) enthält, ist er stärker beteiligt als das vorherige [Beispiel](issuing-the-getnumobjects-command.md).</span><span class="sxs-lookup"><span data-stu-id="2cdad-106">Because this command includes data (or a data phase), it is more involved than the previous [example](issuing-the-getnumobjects-command.md).</span></span> <span data-ttu-id="2cdad-107">Befehle, die eine Daten Phase enthalten, können in drei Teile unterteilt werden:</span><span class="sxs-lookup"><span data-stu-id="2cdad-107">Commands that include a data phase can be broken into three parts:</span></span>

1.  <span data-ttu-id="2cdad-108">Initiierung: die Anwendung initiiert den Befehl, indem das Gerät darüber informiert wird, dass die Daten entweder kommen oder erwartet werden.</span><span class="sxs-lookup"><span data-stu-id="2cdad-108">Initiation: The application initiates the command by informing the device that data is either coming or expected.</span></span>
2.  <span data-ttu-id="2cdad-109">Übertragen: die Anwendung überträgt die Daten (entweder durch Schreiben oder Lesen der Daten).</span><span class="sxs-lookup"><span data-stu-id="2cdad-109">Transfer: The application transfers the data (either by writing or reading the data).</span></span>
3.  <span data-ttu-id="2cdad-110">Abschluss: die Anwendung (oder das Gerät) signalisiert, dass der Befehl abgeschlossen ist, und Ruft einen Antwort Code ab.</span><span class="sxs-lookup"><span data-stu-id="2cdad-110">Completion: The application (or the device) signals that the command is complete and retrieves a response code.</span></span>

<span data-ttu-id="2cdad-111">Die vorherige Liste wird in die folgende Befehlssequenz übersetzt:</span><span class="sxs-lookup"><span data-stu-id="2cdad-111">The previous list translates into the following command sequence:</span></span>

1.  <span data-ttu-id="2cdad-112">WPD- \_ Befehl \_ MTP \_ ext Execute- \_ \_ Befehl \_ mit \_ zu schreibende Daten \_ \_ oder WPD- \_ Befehl \_ MTP \_ ext Execute- \_ \_ Befehl \_ mit \_ \_ zu \_ lesenden Daten.</span><span class="sxs-lookup"><span data-stu-id="2cdad-112">WPD\_COMMAND\_MTP\_EXT\_EXECUTE\_COMMAND\_WITH\_DATA\_TO\_WRITE or WPD\_COMMAND\_MTP\_EXT\_EXECUTE\_COMMAND\_WITH\_DATA\_TO\_READ.</span></span>
2.  <span data-ttu-id="2cdad-113">WPD- \_ Befehl \_ MTP \_ ext Schreiben von \_ \_ Daten oder WPD- \_ Befehl \_ MTP \_ Ext \_ \_ Daten lesen.</span><span class="sxs-lookup"><span data-stu-id="2cdad-113">WPD\_COMMAND\_MTP\_EXT\_WRITE\_DATA or WPD\_COMMAND\_MTP\_EXT\_READ\_DATA.</span></span>
3.  <span data-ttu-id="2cdad-114">WPD- \_ Befehl \_ MTP \_ ext Ende der \_ \_ Daten \_ Übertragung.</span><span class="sxs-lookup"><span data-stu-id="2cdad-114">WPD\_COMMAND\_MTP\_EXT\_END\_DATA\_TRANSFER.</span></span>

<span data-ttu-id="2cdad-115">Im Fall von **setdevicepropvalue** verwendet der Beispielcode die folgende Sequenz:</span><span class="sxs-lookup"><span data-stu-id="2cdad-115">In the case of **SetDevicePropValue**, the sample code uses the following sequence:</span></span>

1.  <span data-ttu-id="2cdad-116">WPD- \_ Befehl \_ MTP \_ ext Execute- \_ \_ Befehl \_ mit \_ \_ zu schreibende Daten \_ .</span><span class="sxs-lookup"><span data-stu-id="2cdad-116">WPD\_COMMAND\_MTP\_EXT\_EXECUTE\_COMMAND\_WITH\_DATA\_TO\_WRITE.</span></span>
2.  <span data-ttu-id="2cdad-117">WPD- \_ Befehl \_ MTP \_ Ext \_ schreibt \_ Daten.</span><span class="sxs-lookup"><span data-stu-id="2cdad-117">WPD\_COMMAND\_MTP\_EXT\_WRITE\_DATA.</span></span>
3.  <span data-ttu-id="2cdad-118">WPD- \_ Befehl \_ MTP \_ ext Ende der \_ \_ Daten \_ Übertragung.</span><span class="sxs-lookup"><span data-stu-id="2cdad-118">WPD\_COMMAND\_MTP\_EXT\_END\_DATA\_TRANSFER.</span></span>

<span data-ttu-id="2cdad-119">Im folgenden Codebeispiel wird gezeigt, wie eine WPD-Anwendung die Befehlssequenz initiiert.</span><span class="sxs-lookup"><span data-stu-id="2cdad-119">The following code example shows how a WPD application initiates the command sequence.</span></span>


```C++
#include <portabledevice.h>
#include <portabledeviceapi.h>
#include <wpdmtpextensions.h>

HRESULT SetDateTime(IPortableDevice* pDevice, LPCWSTR pwszDateTime)
{
    HRESULT hr = S_OK;
    const WORD PTP_OPCODE_SETDEVICEPROPVALUE = 0x1016; 
    const WORD PTP_DEVICEPROPCODE_DATETIME = 0x5011; 
    const WORD PTP_RESPONSECODE_OK = 0x2001;     // 0x2001 indicates command success

    // Build basic WPD parameters for the command
    CComPtr<IPortableDeviceValues> spParameters;
    if (hr == S_OK)
    {
        hr = CoCreateInstance(CLSID_PortableDeviceValues,
                              NULL,
                              CLSCTX_INPROC_SERVER,
                              IID_IPortableDeviceValues,
                              (VOID**)&spParameters);
    }

    // Use WPD_COMMAND_MTP_EXT_EXECUTE_COMMAND_WITH_DATA_TO_WRITE
    if (hr == S_OK)
    {
        hr = spParameters->SetGuidValue(WPD_PROPERTY_COMMON_COMMAND_CATEGORY, 
                                           WPD_COMMAND_MTP_EXT_EXECUTE_COMMAND_WITH_DATA_TO_WRITE.fmtid);
    }

    if (hr == S_OK)
    {
        hr = spParameters->SetUnsignedIntegerValue(WPD_PROPERTY_COMMON_COMMAND_ID, 
                                              WPD_COMMAND_MTP_EXT_EXECUTE_COMMAND_WITH_DATA_TO_WRITE.pid);
    }

    // Specify the actual MTP op-code to execute here
    if (hr == S_OK)
    {
        hr = spParameters->SetUnsignedIntegerValue(WPD_PROPERTY_MTP_EXT_OPERATION_CODE, 
                                                      (ULONG) PTP_OPCODE_SETDEVICEPROPVALUE);
    }

    // SetDevicePropValue requires the property code as an MTP parameter
    // MTP parameters need to be first put into a PropVariantCollection
    CComPtr<IPortableDevicePropVariantCollection> spMtpParams;
    if (hr == S_OK)
    {
        hr = CoCreateInstance(CLSID_PortableDevicePropVariantCollection,
                                  NULL,
                                  CLSCTX_INPROC_SERVER,
                                  IID_IPortableDevicePropVariantCollection,
                                  (VOID**)&spMtpParams);
    }

    PROPVARIANT pvParam = {0};
    pvParam.vt = VT_UI4;

    // Specify the DateTime property as the MTP parameter
    if (hr == S_OK)
    {
        pvParam.ulVal = PTP_DEVICEPROPCODE_DATETIME;
        hr = spMtpParams->Add(&pvParam);
    }

    // Add MTP parameters collection to our main parameter list
    if (hr == S_OK)
    {
        hr = spParameters->SetIPortableDevicePropVariantCollectionValue(
                                          WPD_PROPERTY_MTP_EXT_OPERATION_PARAMS, spMtpParams);
    }  

    // Figure out the data to send - in this case it will be an MTP string
    BYTE* pbBuffer = NULL;
    DWORD cbBufferSize = 0;
    if (hr == S_OK)
    {
        hr = PackString(pwszDateTime, &pbBuffer, &cbBufferSize);
    }

    // Inform the device how much data will arrive - this is a required parameter
    if (hr == S_OK)
    {
        hr = spParameters->SetUnsignedLargeIntegerValue(WPD_PROPERTY_MTP_EXT_TRANSFER_TOTAL_DATA_SIZE, 
                                                        &cbBufferSize);
    }

    // Send the command to initiate the transfer
    CComPtr<IPortableDeviceValues> spResults;
    if (hr == S_OK)
    {
        hr = pDevice->SendCommand(0, spParameters, &spResults);
    }

    // Check if the driver was able to send the command by interrogating WPD_PROPERTY_COMMON_HRESULT
    HRESULT hrCmd = S_OK;
    if (hr == S_OK)
    {
         hr = spResults->GetErrorValue(WPD_PROPERTY_COMMON_HRESULT, &hrCmd);
    }

    if (hr == S_OK)
    {
        printf("Driver return code (initiating): 0x%08X\n", hrCmd);
        hr = hrCmd;
    }

    // The driver returns a context cookie that we need to use during our data transfer
    LPWSTR pwszCookie = NULL;
    if (hr == S_OK)
    {
         hr = spResults->GetStringValue(WPD_PROPERTY_MTP_EXT_TRANSFER_CONTEXT, &pwszContext);
    }
```



<span data-ttu-id="2cdad-120">Im folgenden Codebeispiel wird gezeigt, wie eine WPD-Anwendung die Daten überträgt, nachdem Sie den Befehl initiiert hat.</span><span class="sxs-lookup"><span data-stu-id="2cdad-120">The following code example shows how a WPD application transmits the data after it has initiated the command.</span></span>


```
   // Use the WPD_COMMAND_MTP_EXT_WRITE_DATA command to send the data
    (void) spParameters->Clear();
    if (hr == S_OK)
    {
        hr = spParameters->SetGuidValue(WPD_PROPERTY_COMMON_COMMAND_CATEGORY, 
                                           WPD_COMMAND_MTP_EXT_WRITE_DATA.fmtid);
    }

    if (hr == S_OK)
    {
        hr = spParameters->SetUnsignedIntegerValue(WPD_PROPERTY_COMMON_COMMAND_ID, 
                                                      WPD_COMMAND_MTP_EXT_WRITE_DATA.pid);
    }

    // Specify the same context that we received earlier
    if (hr == S_OK)
    {
        hr = spParameters->SetStringValue(WPD_PROPERTY_MTP_EXT_TRANSFER_CONTEXT, pwszContext);   
    }

    // Specify the number of bytes that arrive with this command. This allows us to 
    // send the data in chunks if required (multiple WRITE_DATA commands). In this case,    //  send the data in a single chunk
    if (hr == S_OK)
    {
        hr = spParameters->SetUnsignedIntegerValue(WPD_PROPERTY_MTP_EXT_TRANSFER_NUM_BYTES_TO_WRITE, 
                                                   cbBufferSize);
    }

    // Provide the data that needs to be transferred
    if (hr == S_OK)
    {
        hr = spParameters->SetBufferValue(WPD_PROPERTY_MTP_EXT_TRANSFER_DATA, pbBuffer, cbBufferSize);
    }

    // Send the data to the device
    spResults = NULL;
    if (hr == S_OK)
    {
        hr = pDevice->SendCommand(0, spParameters, &spResults);
    }

    // Check if the data was sent successfully by interrogating COMMON_HRESULT
    if (hr == S_OK)
    {
         hr = spResults->GetErrorValue(WPD_PROPERTY_COMMON_HRESULT, &hrCmd);
    }

    if (hr == S_OK)
    {
        printf("Driver return code (sending data): 0x%08X\n", hrCmd);
        hr = hrCmd;
    }

    // The driver informs us about the number of bytes that were actually transferred. Normally this
    // should be the same as the number that we provided.
    DWORD cbBytesWritten = 0;
    if (hr == S_OK)
    {
        hr = spResults->GetUnsignedIntegerValue(WPD_PROPERTY_MTP_EXT_TRANSFER_NUM_BYTES_WRITTEN, 
                                                &cbBytesWritten);
    }
```



<span data-ttu-id="2cdad-121">Im folgenden Codebeispiel wird gezeigt, wie eine Anwendung einen Antwort Code vom Gerät abruft.</span><span class="sxs-lookup"><span data-stu-id="2cdad-121">The following code example shows how an application retrieves a response code from the device.</span></span>


```
   // Use the WPD_COMMAND_MTP_EXT_END_DATA_TRANSFER command to signal transfer completion
    (void) spParameters->Clear();
    if (hr == S_OK)
    {
        hr = spParameters->SetGuidValue(WPD_PROPERTY_COMMON_COMMAND_CATEGORY, 
                                           WPD_COMMAND_MTP_EXT_END_DATA_TRANSFER.fmtid);
    }

    if (hr == S_OK)
    {
        hr = spParameters->SetUnsignedIntegerValue(WPD_PROPERTY_COMMON_COMMAND_ID, 
                                                      WPD_COMMAND_MTP_EXT_END_DATA_TRANSFER.pid);
    }

    // Specify the same context that we received earlier
    if (hr == S_OK)
    {
        hr = spParameters->SetStringValue(WPD_PROPERTY_MTP_EXT_TRANSFER_CONTEXT, pwszContext);   
    }

    // Send the completion command
    spResults = NULL;
    if (hr == S_OK)
    {
        hr = pDevice->SendCommand(0, spParameters, &spResults);
    }

    // Check if the driver successfully ended the data transfer
    if (hr == S_OK)
    {
         hr = spResults->GetErrorValue(WPD_PROPERTY_COMMON_HRESULT, &hrCmd);
    }

    if (hr == S_OK)
    {
        printf("Driver return code (ending transfer): 0x%08X\n", hrCmd);
        hr = hrCmd;
    }

    // If the command was executed successfully, check the MTP response code to see if the
    // device can handle the command and the data. Be aware that there is a distinction between the command
    // and the data being successfully sent to the device and the command and data being handled successfully 
    // by the device
    DWORD dwResponseCode;
    if (hr == S_OK)
    {
        hr = spResults->GetUnsignedIntegerValue(WPD_PROPERTY_MTP_EXT_RESPONSE_CODE, &dwResponseCode);
    }

    if (hr == S_OK)
    {
        printf("MTP Response code: 0x%X\n", dwResponseCode);
        hr = (dwResponseCode == (DWORD) PTP_RESPONSECODE_OK) ? S_OK : E_FAIL;
    }

    // If response parameters are present, they will be contained in the WPD_PROPERTY_MTP_EXT_RESPONSE_PARAMS 
    // property. SetDevicePropValue does not return additional response parameters, so skip this code 
    

    // Free up any allocated memory
    CoTaskMemFree(pbBuffer);
    CoTaskMemFree(pwszContext);

    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="2cdad-122">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="2cdad-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2cdad-123">Unterstützen von MTP-Erweiterungen</span><span class="sxs-lookup"><span data-stu-id="2cdad-123">Supporting MTP Extensions</span></span>](supporting-mtp-extensions.md)
</dt> </dl>

 

 



